---
layout: post
title: 人工智能正在碾压人类，这不是科幻
categories: [Heroes, Translation]
---

本文因黄仁勋在 [VentureBeat 专访](http://venturebeat.com/2016/11/13/nvidias-ceo-on-everything-from-ais-dangers-to-donald-trump-and-the-nintendo-switch/)中的一段话有感而发，毕竟“人工智能正在以各种各样的方式渗透进人们的生活”：

> “我不需要科幻（也能了解未来的样子），因为我当下就处在科幻之中。我们公司已经相当接近科幻作品所能描述的那些先进技术了。虚拟现实、人工智能、机器人，这些我们正在研发的技术，足以让我们切身体验到那样的科幻场景。”

行文着重参考了黄仁勋的两篇博客（[智能工业革命](https://blogs.nvidia.com/blog/2016/10/24/intelligent-industrial-revolution/)、[GPU 为人工智能加速:崭新的计算模型](https://blogs.nvidia.com/blog/2016/01/12/accelerating-ai-artificial-intelligence-gpus/)），以及 Tim Urban 那两篇 [人工智能革命](http://bitandliteracy.github.io/AI-Revolution)。

***

在人工智能领域，有一句古老的说法：

> **“一旦一样东西用人工智能实现了，人们就不再叫它人工智能了。”**

比如 Google 的搜索与翻译、苹果的 Siri、手机常用的地图导航、邮箱里的垃圾邮件过滤、汽车上的防抱死系统……诸如此类的功能，我们一般都不会称它们为人工智能。

因为，在我们看来，这样的功能实在是太稀松平常了。

毕竟，在那些人或动物不需要思考就能完成的事情上，人工智能还差得很远。

可事实却是，在几乎所有都需要进行思考的领域，人工智能都已经超越了人类。

![]({{ site.baseurl }}/images/AI-progressing-01.jpg)

特别是世界上最耗脑力的棋类比赛，无论围棋、象棋还是黑白棋，最强的选手已经属于人工智能了。

不仅如此，随着近年来人工智能技术的发展，在原本毫无胜算的那些事情上，人工智能也开始接近或超越人类的水平。

## 意外的突破

2012年，一个名不见经传的多伦多大学研究生 Alex Krizhevsky，创建了一个能够从一百万个样本中自动学习识别图像的深度神经网络「AlexNet」。仅经过几天的训练，「AlexNet」就赢得了那一年的 ImageNet 计算机图像识别比赛，打败了人类专家们磨炼了几十年的所有算法。

![]({{ site.baseurl }}/images/AI-progressing-02.jpg)

`「ImageNet」比赛用的数据集`

这里最有趣的一点是，尽管「AlexNet」所采用的正是卷积神经网络，但卷积神经网络的发明人却无法重现「AlexNet」的结果。这让该发明人大为震动，他立刻组织会议去反思：

> **“为什么过去两年我们没有得到这样的成绩？”**

不过，受到震动的不止是学术界，整个人工智能产业界同样大为震惊，特别是在人才和资源均不受限制的 Google Brain 团队。

因为 ImageNet 大赛期间，采用一样的数据集，Google Brain 团队同样用深度学习做了非公开的测试，但识别精度相比「AlexNet」的可要差多了。

人工智能业界的神话——Jeff Dean、吴恩达等人，顿时脸面无光。

![]({{ site.baseurl }}/images/AI-progressing-03.jpg)

`「AlexNet」三人组：最远为 Alex Krizhevsky`

围绕“深度学习”的人才争夺战随即拉开。不久，Google 不惜血本收购了「AlexNet」的团队，以5000万美元买下这个团队的部分研究时间。没能抢到人才的 Facebook，转而挖走卷积神经网络的发明人。吴恩达则离开 Google 去了百度。

## 毛头小子如何打败业界神话

要知道，Google Brain 团队有着整个业界所无法企及的硬件和数据资源支持，它独自享有一个完整的 Google 巨型数据中心，该中心的服务器上安装了2000个企业级的 CPU。

这种规模的计算能力带来了惊人的研究成果，Google Brain 通过观看 YouTube 上的视频就能学会辨别其中的猫和人。

而「AlexNet」的硬件仅仅是英伟达的 GTX 580 显卡，为什么呢？

![]({{ site.baseurl }}/images/AI-progressing-04.jpg)

`GTX 580 显卡`

于是，英伟达研究中心与吴恩达就在斯坦福大学展开合作，使用大型 GPU 计算系统来开发训练神经网络的方法，以研究更大的网络、更大的大脑、更多的学习。

结果表明，**12 个英伟达 GPU 的深度学习能力相当于 2000 个 CPU 的表现。**

《自然》杂志则指出，「GPU 让研究人员将训练神经网络的速度提高了 10 到 20 倍」，将每项训练迭代时间从几周减少到几天，而 GPU 的综合性能、编程生产力及公开访问性等因素对打造新的计算平台非常重要。

![]({{ site.baseurl }}/images/AI-progressing-05.jpg)

`Google 数据中心`

此后，所有重大的人工智能开发框架均采用英伟达的 GPU 来加快计算速度，从互联网公司到研究机构，再到新创公司。仅仅三年，深度神经网络的训练速度就提升了 50 倍。

可以说，GPU 计算的崛起，拉开了人工智能突飞猛进的序幕。

## 超越人类水平

随后，深度学习技术方面，计算机的感知理解能力在某一方面「超越人类水平」的消息不断出现：

+ Google 与微软均使用深度学习，在 ImageNet 竞赛上打破了人类所创造的最好成绩（注意：不是打败人类所编写的程序，而是打败人类）。
+ 微软和中国科技大学宣布他们开发的 DNN 达到了大学毕业生的智商测试分数。
+ 微软研究院使用 GPU 深度学习使对话语音达到了和人类相同的水准，实现了历史性的里程碑。

当然，最具标志性的事件，还是 Google 的 Alpha Go 在围棋上击败李世石。

![]({{ site.baseurl }}/images/AI-progressing-06.jpg)

接下来，让我们简单回顾一下这些达到或超越人类水平的人工智能：

#### Google Brain

![]({{ site.baseurl }}/images/AI-progressing-07.jpg)

`Google Brain 画作`

除了 Alpha Go，Google Brain 的 “Magenta” 项目，正在探索用人工智能来进行艺术创作，写诗、作曲、绘画、拍电影无所不能，它的画作甚至还拍卖出了8000美元。

而经深度学习改造后的 Google 翻译，已接近人类笔译的水平，错误率减少了60%。

最近，Google Brain 的神经网络之间，不仅可以相互交流，甚至还能对交流的信息进行加密。

#### 语音识别

![]({{ site.baseurl }}/images/AI-progressing-08.jpg)

`百度 Deep Speech `

8月份，百度、斯坦福与华盛顿大学的一项关于智能手机输入方式的对比研究表明，智能手机使用百度 Deep Speech 2 的语音输入，速度要比手动的键盘输入快3倍，且准确率更高。

10月中旬，微软人工智能与研究部门的团队说，他们的语音识别系统的词错率低至5.9%，相当于人类专业速录员的水平。这意味着，计算机第一次在对话中的词汇识别上做到跟人类一样好。

#### IBM Watson

![]({{ site.baseurl }}/images/AI-progressing-09.jpg)

2011年，Watson 在电视智力竞赛节目《危险边缘》中打败人类选手，一战成名。

Watson 最近的战绩是为科幻影片《摩根》制作预告片，并编辑了一期 The Drum 杂志。

在 IBM 主打的医疗健康领域，Watson 已能根据病人的 DNA 指纹开展基因治疗，东京大学还利用 Watson 成功治愈了一位 60 岁的白血病患者。

#### 自动驾驶

![]({{ site.baseurl }}/images/AI-progressing-10.jpg)

Tesla 最新发布的具备完全自动驾驶功能的 Autopilot 硬件，将为汽车提供一个人类司机无法用肉眼观测的周边世界的完整全景信息图，让自动驾驶系统能够做出更安全的决策。

其中用来处理各个传感器传输来的图像、声纳和雷达信号的，是基于英伟达 Titan 显卡的特斯拉神经网络，目标是实现比人类司机安全10倍的自动驾驶体验。

![]({{ site.baseurl }}/images/AI-progressing-11.jpg)

诸如此类的人工智能技术，也许就像地球早期软泥中的氨基酸——表面上波澜不惊，可眨眼之间就能组成生命。

而英伟达 CEO 黄仁勋还认为，人工智能的发展会比摩尔定律更快，换言之，超越人类的人工智能也将来临得更快。

想象一下全面超越人类的人工智能：比你感知得更多更准，比你思考得更快更深，以一种远超你所能理解的能力来操纵于你、摆布世界，就像生、老、病、死的自然规律那样……我们改天可以详谈这方面的话题。

![]({{ site.baseurl }}/images/AI-progressing-12.jpg)

## 超越摩尔定律？

但短期内，世界会存在无数的人工智能系统，有的擅长营销、有的擅长供应链、有的擅长预测、有的擅长人力资源……它们很快就会加入到我们目前所用的各类软件和应用之中，而且不用担心，它们在自己的领域肯定要比你更擅长。

因为人工智能具有大规模网络化持续学习的特点，它必然会受益于持续地学习，从而成为一种超越摩尔定律的现象。

正在发展中的虚拟现实、人工智能和机器人技术，已经让我们亲身体验到科幻小说中的场景。那么，人工智能统治世界的科幻情节还会远吗？

***

注：本文曾作为 [人工智能正在碾压人类，这可不是科幻片里的剧情](http://mp.weixin.qq.com/s/6JzWHnDix1fb4119RaR-9A) 发表在「极客视界」微信号，获得众多评论。

参考来源：

+ [Accelerating AI with GPUs: A New Computing Model](https://blogs.nvidia.com/blog/2016/01/12/accelerating-ai-artificial-intelligence-gpus/)（[中文](http://blogs.nvidia.cn/2016/01/accelerating-ai-artificial-intelligence-gpus/)）
+ [The Intelligent Industrial Revolution](https://blogs.nvidia.com/blog/2016/10/24/intelligent-industrial-revolution/)（[翻译](http://www.jiqizhixin.com/article/1720)）
+ [Nvidia’s CEO discusses AI dangers, Donald Trump, the Nintendo Switch, and more](http://venturebeat.com/2016/11/13/nvidias-ceo-on-everything-from-ais-dangers-to-donald-trump-and-the-nintendo-switch/)（[翻译](http://www.jiqizhixin.com/article/1812)）