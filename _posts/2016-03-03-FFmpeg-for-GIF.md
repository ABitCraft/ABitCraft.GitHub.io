---
layout: post
title: 尝试用 FFmpeg 来生成 GIF 图
---
由于工作上每天都要制作不少 GIF 图，所以用过很久 Photoshop, LICEcap, GIF Brewery 等 GUI 工具。直到最近读到这篇（[High quality GIF with FFmpeg](http://blog.pkh.me/p/21-high-quality-gif-with-ffmpeg.html)，即 [使用 FFmpeg 处理高质量 GIF 图片](http://www.oschina.net/translate/high-quality-gif-with-ffmpeg)）通过 FFmpeg 来输出 GIF 图的文章，我决定去尝试一下用命令行的方式来生成 GIF 图效果。

*习惯于用参数的话，还是能省心不少的。*

***

## 安装 FFmpeg

既然要使用 [FFmpeg](http://ffmpeg.org), 第一步自然是先安装好 FFmpeg。

[How to install FFmpeg on Mac OS X](http://www.renevolution.com/how-to-install-ffmpeg-on-mac-os-x/) 一文介绍的是，Mac 可以在 [Homebrew](http://mxcl.github.com/homebrew/) 下直接安装 FFmepg: `brew install ffmpeg [all your options]`，具体的命令是：

> 1. 查看所有可用选项： `brew options ffmpeg`
>
> 2. 用所有可用参数完整安装是这个命令：
<pre><code>brew install ffmpeg --with-fdk-aac --with-ffplay --with-freetype --with-frei0r --with-libass --with-libvo-aacenc --with-libvorbis --with-libvpx --with-opencore-amr --with-openjpeg --with-opus --with-rtmpdump --with-schroedinger --with-speex --with-theora --with-tools</code></pre>

*在搞定 10.11 的 Homebrew 之前，我是去下载已编译好的 [FFmpeg 二进制文件](http://evermeet.cx/ffmpeg/)，然后直接放入 `/usr/Local/bin` 目录下来使用的。*

## 使用 FFmpeg

FFmpeg 文档中生成 GIF 图的命令非常简单：

`ffmpeg -i input.mkv -i palette.png -lavfi paletteuse output.gif `

对 GIF 图效果有要求的话，`使用 FFmpeg 处理高质量 GIF 图片` 一文所提供的命令是这样的：

`./gifenc.sh video.mkv anim.gif`

所用的 shell 脚本如下：

<pre><code>#!/bin/sh

start_time=12:23
duration=35

palette="/tmp/palette.png"

filters="fps=15,scale=320:-1:flags=lanczos"

ffmpeg -v warning -ss $start_time -t $duration -i $1 -vf "$filters,palettegen" -y $palette
ffmpeg -v warning -ss $start_time -t $duration -i $1 -i $palette -lavfi "$filters [x]; [x][1:v] paletteuse" -y $2
</code></pre>

使用这个 FFmpeg 脚本所生成的 GIF 图效果确实不错，但我希望能通过命令参数来指定 GIF 图的开始时间和时长，以及分辨率、帧率、色彩位数等因素，从而能更加灵活地使用命令行来制作 GIF 图。

于是修改出来的脚本就是这样：

<pre><code>#!/bin/sh

GIF="$2.gif"

start_time=$3
duration=$4

palette="palette.png"

filters="fps=$5,scale=$6:-1:flags=lanczos"

ffmpeg -v warning -ss $start_time -t $duration -i $1 -vf "$filters,palettegen=max_colors=$7:stats_mode=diff" -y $palette
ffmpeg -v warning -ss $start_time -t $duration -i $1 -i $palette -lavfi "$filters [x]; [x][1:v] paletteuse=dither=floyd_steinberg" -y $GIF
</code></pre>

这时输入到终端里面的命令就变成：

`./gifenc.sh input.mkv output 75 6 10 640 128 `

其中的 $1 `input.mkv` 是完整的视频文件名 ，$2 `output` 则是 GIF 图名字，$3 `75`秒 是指开始时间，$4 `6`秒 表示 GIF 图时长为 ，$5  `10`fps 即 GIF 图帧率，$6 `480`像素即 GIF 图宽度，$7 `128` 表示 GIF 图色彩位数`[4-256]`。

尽管这看上去比较复杂，但制作 GIF 图时的效率着实提升显著，性能较差的电脑也足以胜任。

## 另外，关于 Windows 系统

参考 [如何在Windows上安装FFmpeg程序](http://zh.wikihow.com/在Windows上安装FFmpeg程序) 。

下载 [Windows 版程序](http://ffmpeg.zeranoe.com/builds/)，设置好 PATH 环境变量即可。

Windows 批处理的参数是以 `%` 而非 `$` 开头，变量则需在末尾也加上 `%`，因而只需把 shell 脚本作相应的修改即可使用：

<pre><code>set GIF="%2.gif"
set start_time=%3
set duration=%4

set palette="palette.png"

set filters="fps=%5,scale=%6:-1:flags=lanczos"

ffmpeg -v warning -ss %start_time% -t %duration% -i %1 -vf "%filters%,palettegen=max_colors=%7:stats_mode=diff" -y %palette%
ffmpeg -v warning -ss %start_time% -t %duration% -i %1 -i %palette% -lavfi "%filters% [x]; [x][1:v] paletteuse=dither=floyd_steinberg" -y %GIF%
</code></pre>

相应的命令行指令也改为：

`gifenc.bat input.mkv output 75 6 10 640 128 `

***

后来把 FFmpeg 的这个用法告诉我们自己的小编，他一口气做了 10 多张 GIF 图，尽管手里的文章仅用上 8 张：

`“电脑不卡的时候做 GIF 图还是很爽的。”`

既然还算管用……我们就把寻找这个工具的过程分享出来，希望能帮上某个还没用上它的人。