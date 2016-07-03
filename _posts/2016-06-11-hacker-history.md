---
layout: posts
title: 黑客圈简史
categories: Hackerdom
---

> 本文是 ESR 的 [A Brief History of Hackerdom](http://www.catb.org/esr/writings/homesteading/hacker-history/)，译文内容来自 LUPAworld 的 [Eric S. Raymond 五部曲](http://man.lupaworld.com/content/develop/joyfire/project/7.html) 文档，以后我会完善这份文档的翻译。

***

**Eric Steven Raymond**

[Thyrsus Enterprises](http://www.tuxedo.org/~esr/)

<esr@thyrsus.com>

版本 1.24

Copyright © 2000 Eric S. Raymond

**Copyright**

允许以 Open Publication License（开放出版协议）`version 2.0` ，复制、分发 `和/或` 修改本文档。

$Date: 2002/08/02 08:21:12 $

<div class="row">
<div class="span2">
<table class="table table-bordered table-striped table-condensed">
<tr><th align="left" colspan="3">版本历史</th></tr>
<tr><td align="left">版本 1.24</td><td align="right">25 August 2000</td><td align="right">esr</td></tr>
<tr><td align="left" colspan="3">First DocBook version.</td></tr>
<tr><td align="left">版本 1.23</td><td align="right">29 Dec 1999</td><td align="right">esr</td></tr>
<tr><td align="left" colspan="3">This version went into the first printed edition.</td></tr>
<tr><td align="left">版本 1.20</td><td align="right">17 August 1999</td><td align="right">esr </td></tr>
<tr><td align="left" colspan="3">First SGML version with bibliography.</td></tr>
<tr><td align="left">版本 1.1</td><td align="right">15 Feb 1997</td><td align="right">esr </td></tr>
<tr><td align="left" colspan="3">This document dates from around 1992, but was not version-controlled until 1997.</td></tr>
</table>
</div>
</div>

**目录**

* 黑客圈简史
{:toc}

## 简介

I explore the origins of the hacker culture, including prehistory among the Real Programmers, the glory days of the MIT hackers, and how the early ARPAnet nurtured the first network nation. I describe the early rise and eventual stagnation of Unix, the new hope from Finland, and how `the last true hacker' became the next generation's patriarch. I sketch the way Linux and the mainstreaming of the Internet brought the hacker culture from the fringes of public consciousness to its current prominence.


***

## 序曲：Real Programmer

In the beginning, there were Real Programmers.
故事一开始，我要介绍的是所谓的Real Programmer。

That's not what they called themselves. They didn't call themselves `hackers', either, or anything in particular; the sobriquet `Real Programmer' wasn't coined until after 1980, retrospectively by one of their own. But from 1945 onward, the technology of computing attracted many of the world's brightest and most creative minds. From Eckert and Mauchly's first ENIAC computer onward there was a more or less continuous and self-conscious technical culture of enthusiast programmers, people who built and played with software for fun.
他们从不自称是Real Programmer、Hacker或任何特殊的称号；`Real Programmer' 这个名词是在1980年代才出现，但早自1945年起，电脑科学便不断地吸引世界上头脑最顶尖、想像力最丰富的人投入其中。从Eckert &Mauchly发明ENIAC後，便不断有狂热的programmer投入其中，他们以撰写软件与玩弄各种程式设计技巧为乐，逐渐形成具有自我意识的一套科技文化。

The Real Programmers typically came out of engineering or physics backgrounds. They were often amateur-radio hobbyists. They wore white socks and polyester shirts and ties and thick glasses and coded in machine language and assembler and FORTRAN and half a dozen ancient languages now forgotten.
当时这批Real Programmers主要来自工程界与物理界，他们戴著厚厚的眼镜， 穿聚酯纤维T恤与纯白袜子，用机器语言、汇编语言、FORTRAN及很多古老的 语言写程式。他们是Hacker时代的先驱者，默默贡献，却鲜为人知。

From the end of World War II to the early 1970s, in the great days of batch processing and the ``big iron'' mainframes, the Real Programmers were the dominant technical culture in computing. A few pieces of revered hacker folklore date from this era, including various lists of Murphy's Laws and the mock-German ``Blinkenlights'' poster that still graces many computer rooms.
从二次大战结束後到1970早期，是打卡计算机与所谓"大铁块"的mainframes 流行的年代，由Real Programmer主宰电脑文化。Hacker传奇故事如有名的 Mel (收录在Jargon File中)、Murphy's Law的各种版本、mock- German`Blinke_nlight' 文章都是流传久远的老掉牙笑话了。

Some people who grew up in the `Real Programmer' culture remained active into the 1990s and even past the turn of the 21st century. Seymour Cray, designer of the Cray line of supercomputers, was among the greatest. He is said once to have toggled an entire operating system of his own design into a computer of his own design through its front-panel switches. In octal. Without an error. And it worked. Real Programmer macho supremo. 一些Real Programmer仍在世且十分活跃 (本文写在1996年)。超级电脑Cray 的设计者Seymour Cray， 据说亲手设计Cray全部的硬体与其操作系统，作业系统是他用机器码硬干出来的，没有出过任何bug或error。Real Programmer 真是超强！

The `Real Programmer' culture, though, was heavily associated with batch (and especially batch scientific) computing. It was eventually eclipsed by the rise of interactive computing, the universities, and the networks. These gave birth to another engineering tradition that, eventually, would evolve into today's open-source hacker culture.
Real Programmer的时代步入尾声，取而代之的是逐渐盛行的Interactive computing，大学成立电算相关科系及电脑网络。它们催生了另一个持续的工程传统，并最终演化为今天的开放代码黑客文化。

## 早期的黑客

The beginnings of the hacker culture as we know it today can be conveniently dated to 1961, the year MIT acquired the first PDP-1. The Signals and Power Committee of MIT's Tech Model Railroad Club adopted the machine as their favorite tech-toy and invented programming tools, slang, and an entire surrounding culture that is still recognizably with us today. These early years have been examined in the first part of Steven Levy's book Hackers [Levy].
Hacker时代的滥觞始於1961年MIT出现第一台电脑DEC PDP-1。MIT的Tech Model Railroad Club(简称TMRC)的Power and Signals Group买了这台机器後，把它当成最时髦的科技玩具，各种程式工具与电脑术语开始出现，整个环境与文化一直发展下去至今日。 这在Steven Levy的书`Hackers' 前段有详细的记载(Anchor/Doubleday 公司，1984年出版

MIT's computer culture seems to have been the first to adopt the term `hacker'. The Tech Model Railroad Club's hackers became the nucleus of MIT's Artificial Intelligence Laboratory, the world's leading center of AI research into the early 1980s. Their influence was spread far wider after 1969, the first year of the ARPAnet.

The ARPAnet was the first transcontinental, high-speed computer network. It was built by the Defense Department as an experiment in digital communications, but grew to link together hundreds of universities and defense contractors and research laboratories. It enabled researchers everywhere to exchange information with unprecedented speed and flexibility, giving a huge boost to collaborative work and tremendously increasing both the pace and intensity of technological advance.
ARPANET是第一个横跨美国的高速网络。由美国国防部所出资兴建，一个实验性 质的数位通讯网络，逐渐成长成联系各大学、国防部承包商及研究机构的大网络。 各地研究人员能以史无前例的速度与弹性交流资讯， 超高效率的合作模式导致科技 的突飞猛进。

But the ARPAnet did something else as well. Its electronic highways brought together hackers all over the U.S. in a critical mass; instead of remaining in isolated small groups each developing their own ephemeral local cultures, they discovered (or re-invented) themselves as a networked tribe.
ARPANET另一项好处是，资讯高速公路使得全世界的hackers能聚在一起，不再像以前孤立在各地形成一股股的短命文化，网络把他们汇流成一股强大力量。 开始有人感受到Hacker文化的存在，动手整理术语放上网络， 在网上发表讽刺文学与讨论Hacker所应有的道德规范。(Jargon File的第一版出现在1973年，就是一个好例子)， Hacker文化在有接上ARPANET的各大学间快速发展，特别是(但不全是)在信息相关科系。

The first intentional artifacts of the hacker culture—the first slang lists, the first satires, the first self-conscious discussions of the hacker ethic—all propagated on the ARPAnet in its early years. In particular, the first version of the Jargon File developed as a cross-net collaboration during 1973–1975. This slang dictionary became one of the culture's defining documents. It was eventually published as "The Hacker's Dictionary" in 1983; that first version is out of print, but a revised and expanded version is New Hacker's Dictionary [Raymond].

Hackerdom flowered at the universities connected to the net, especially (though not exclusively) in their computer science departments. MIT's AI and LCS labs made it first among equals from the late 1960s. But Stanford University's Artificial Intelligence Laboratory (SAIL) and Carnegie-Mellon University (CMU) became nearly as important. All were thriving centers of computer science and AI research. All attracted bright people who contributed great things to the hacker culture, on both the technical and folkloric levels.
一开始，整个Hacker文化的发展以MIT的AI Lab为中心，但Stanford University 的Artificial Intelligence Laboratory(简称SAIL)与稍後的Carnegie-Mellon University(简称CMU)正快速崛起中。 三个都是大型的资讯科学研究中心及人工智慧的权威，聚集著世界各地的精英，不论在技术上或精神层次上，对Hacker文化都有极高的贡献。

To understand what came later, though, we need to take another look at the computers themselves; because the AI Lab's rise and its eventual fall were both driven by waves of change in computing technology.
为能了解後来的故事，我们得先看看电脑本身的变化；随著科技的进步，主角MIT AI Lab也从红极一时到最後淡出舞台。

Since the days of the PDP-1, hackerdom's fortunes had been woven together with Digital Equipment Corporation's PDP series of minicomputers. DEC pioneered commercial interactive computing and time-sharing operating systems. Because their machines were flexible, powerful, and relatively cheap for the era, lots of universities bought them.
从MIT那台PDP-1开始，Hacker们主要程式开发平台都是Digital Equipment Corporation 的PDP迷你电脑序列。DEC率先发展出商业用途为主的interactive computing及time-sharing操作系统，当时许多的大学都是买DEC的机器， 因为它兼具弹性与速度，还很便宜(相对於较快的大型电脑mainframe)。

Cheap time-sharing was the medium the hacker culture grew in, and for most of its lifespan the ARPAnet was primarily a network of DEC machines. The most important of these was the PDP-10, first released in 1967. The 10 remained hackerdom's favorite machine for almost fifteen years; TOPS-10 (DEC's operating system for the machine) and MACRO-10 (its assembler) are still remembered with nostalgic fondness in a great deal of slang and folklore.
 便宜的分时系统是Hacker文化能快速成长因素之一，在PDP流行的时代， ARPANET上是DEC机器的天下，其中最重要的便属PDP-10，PDP-10受到Hacker们的青睐达十五年；TOPS-10(DEC的操作系统)与MACRO-10(它的组译器)，许多怀旧的术语及Hacker传奇中仍常出现这两个字。

MIT, though it used the same PDP-10s as everyone else, took a slightly different path; they rejected DEC's software for the PDP-10 entirely and built their own operating system, the fabled ITS.
MIT像大家一样用PDP-10，但他们不屑用DEC的操作系统。他们偏要自己写一个：传说中赫赫有名的ITS。

ITS stood for `Incompatible Time-sharing System' which gives one a pretty good fix on the MIT hackers' attitude (technically, the name was a play on its predecessor, the Compatible Time-Sharing System CTSS). They wanted it their way. Fortunately for all, MIT's people had the intelligence to match their arrogance. ITS, quirky and eccentric and occasionally buggy though it always was, hosted a brilliant series of technical innovations and still arguably holds the record as the single time-sharing system in longest continuous use.
ITS全名是`Incompatible Timesharing System'，取这个怪名果然符合MIT的搞怪作风 -- 就是要与众不同， 他们很臭屁但够本事自己去写一套操作系统。ITS始终不稳，设计古怪，bug也不少，但仍有许多独到的创见，似乎还是分时系统中开机时间最久的纪录保持者。

ITS itself was written in assembler, but many ITS projects were written in the AI language LISP. LISP was far more powerful and flexible than any other language of its day; in fact, it is still a better design than most languages of today, twenty-five years later. LISP freed ITS's hackers to think in unusual and creative ways. It was a major factor in their successes, and remains one of hackerdom's favorite languages.
ITS本身是用汇编语言写的，其他部分由LISP写成。LISP在当时是一个威力强大与极具弹性的程式语言；事实上，二十五年後的今天，它的设计仍优於目前大多数的程式语言。LISP让ITS的Hacker得以尽情发挥想像力与搞怪能力。LISP是MIT AI Lab成功的最大功臣，现在它仍是Hacker们的最爱之一。

Many of the ITS culture's technical creations are still alive today; the EMACS program editor is perhaps the best-known. And much of ITS's folklore is still `live' to hackers, as one can see in the Jargon File.
很多ITS的产物到现在仍活著；EMACS大概是最有名的一个，而ITS的稗官野史仍为今日的Hacker们所津津乐道， 就如同你在Jargon File中所读到的一般。在MIT红得发紫之际，SAIL与CMU也没闲著。SAIL的中坚份子後来成为PC 界或图形使用者介面研发的要角。CMU的Hacker则开发出第一个实用的大型专 家系统与工业用机器人。

SAIL and CMU weren't asleep, either. Many of the cadre of hackers that grew up around SAIL's PDP-10 later became key figures in the development of the personal computer and today's window/icon/mouse software interfaces. Meanwhile hackers at CMU were doing the work that would lead to the first practical large-scale applications of expert systems and industrial robotics.

Another important node of the culture was XEROX PARC, the famed Palo Alto Research Center. For more than a decade, from the early 1970s into the mid-1980s, PARC yielded an astonishing volume of groundbreaking hardware and software innovations. The modern mice, windows, and icons style of software interface was invented there. So was the laser printer, and the local-area network; and PARC's series of D machines anticipated the powerful personal computers of the 1980s by a decade. Sadly, these prophets were without honor in their own company; so much so that it became a standard joke to describe PARC as a place characterized by developing brilliant ideas for everyone else. Their influence on hackerdom was pervasive.
另一个Hacker重镇是XEROX PARC公司的Palo Alto Research Center。从 1970初期到1980中期这十几年间，PARC不断出现惊人的突破与发明，不论质或量，软件或硬体方面。如现今的视窗滑鼠介面，雷射印表机与区域网络； 其D系列的机器，催生了能与迷你电脑一较长短的强力个人电脑。不幸这群先知先觉者并不受到公司高层的赏识；PARC是家专门提供好点子帮别人赚钱的公司成为众所皆知的大笑话。即使如此，PARC这群人对Hacker文化仍有不可抹灭的贡献。

The ARPAnet and the PDP-10 cultures grew in strength and variety throughout the 1970s. The facilities for electronic mailing lists that had been used to foster cooperation among continent-wide special-interest groups were increasingly also used for more social and recreational purposes. DARPA deliberately turned a blind eye to all the technically `unauthorized' activity; it understood that the extra overhead was a small price to pay for attracting an entire generation of bright young people into the computing field.
1970年代与PDP-10文化迅速成长茁壮。Mailing list的出现使世界各地的人得以组成许多SIG(Special-interest group)，不只在电脑方面，也有社会与娱乐方面的。DARPA对这些非`正当性'活动睁一只眼闭一只眼， 因为靠这些活动会吸引更多的聪明小夥子们投入电脑领域呢。

Perhaps the best-known of the `social' ARPAnet mailing lists was the SF-LOVERS list for science-fiction fans; it is still very much alive today, in fact, on the larger `Internet' that ARPAnet evolved into. But there were many others, pioneering a style of communication that would later be commercialized by for-profit time-sharing services like CompuServe, GEnie and Prodigy (and later still dominated by AOL).
有名的非电脑技术相关的ARPANET mailing list首推科幻小说迷的，时至今日ARPANET变成Internet， 愈来愈多的读者参与讨论。Mailing list逐渐成为一种公众讨论的媒介，导致许多商业化上网服务如CompuServe、Genie与Prodigy的成立。

Your historian first became involved with the hacker culture in 1977 through the early ARPAnet and science-fiction fandom. From then onward, I personally witnessed and participated in many of the changes described here.

## Unix 的兴起

Far from the bright lights of the ARPAnet, off in the wilds of New Jersey, something else had been going on since 1969 that would eventually overshadow the PDP-10 tradition. The year of ARPAnet's birth was also the year that a Bell Labs hacker named Ken Thompson invented Unix.
此时在新泽西州的郊外，另一股神秘力量积极入侵Hacker社会，终於席卷整个PDP-10的传统。它诞生在1969年，也就是ARPANET成立的那一年，有个在AT&T Bell Labs的年轻小夥子Ken Thompson发明了Unix。

Thompson had been involved with the development work on a time-sharing OS called Multics, which shared common ancestry with ITS. Multics was a test-bed for some important ideas about how the complexity of an operating system could be hidden inside it, invisible to the user, and even to most programmers. The idea was to make using Multics from the outside (and programming for it!) much simpler, so that more real work could get done.
Thomspon曾经参与Multics的开发，Multics是源自ITS的操作系统，用来实做当时一些较新的OS理论， 如把操作系统较复杂的内部结构隐藏起来，提供一个介面，使的programmer能不用深入了解操作系统与硬体设备，也能快速开发程式。

Bell Labs pulled out of the project when Multics displayed signs of bloating into an unusable white elephant (the system was later marketed commercially by Honeywell but never became a success). Ken Thompson missed the Multics environment, and began to play at implementing a mixture of its ideas and some of his own on a scavenged DEC PDP-7.
在发现继续开发Multics是做白工时，Bell Labs很快的退出了(後来有一家公司Honeywell出售Multics，赔的很惨)。Ken Thompson很喜欢Multics上的作业环境，於是他在实验室里一台报废的DEC PDP-7上胡乱写了一个操作系统，  该系统在设计上有从Multics抄来的也有他自己的构想。他将这个操作系统命名Unix，用来反讽Multics。

Another hacker named Dennis Ritchie invented a new language called `C' for use under Thompson's embryonic Unix. Like Unix, C was designed to be pleasant, unconstraining, and flexible. Interest in these tools spread at Bell Labs, and they got a boost in 1971 when Thompson and Ritchie won a bid to produce what we'd now call an office automation system for internal use there. But Thompson & Ritchie had their eye on a bigger prize.
他的同事Dennis Ritchie，发明了一个新的程式语言C，於是他与Thompson用C把原来用汇编语言写的Unix重写一遍。C的设计原则就是好用，自由与弹性，C与Unix很快地在Bell Labs得到欢迎。1971年Thompson与Ritchie争取到一个办公室自动化系统的专案，Unix开始在Bell Labs中流行。不过Thompson与Ritchie的雄心壮志还不止於此。

Traditionally, operating systems had been written in tight assembler to extract the absolute highest efficiency possible out of their host machines. Thompson and Ritchie were among the first to realize that hardware and compiler technology had become good enough that an entire operating system could be written in C, and by 1978 the whole environment had been successfully ported to several machines of different types.
那时的传统是，一个操作系统必须完全用汇编语言写成，始能让机器发挥最高的效能。Thompson与Ritchie， 是头几位领悟硬体与编译器的技术，已经进步到作业系统可以完全用高阶语言如C来写，仍保有不错的效能。五年後， Unix已经成功地移植到数种机器上。

This had never been done before, and the implications were enormous. If Unix could present the same face, the same capabilities, on machines of many different types, it could serve as a common software environment for all of them. No longer would users have to pay for complete new designs of software every time a machine went obsolete. Hackers could carry around software toolkits between different machines, rather than having to re-invent the equivalents of fire and the wheel every time.
这当时是一件不可思议的事！它意味著，如果Unix可以在各种平台上跑的话，Unix 软件就能移植到各种机器上。再也用不著为特定的机器写软件了，能在Unix上跑最重要，重新发明轮子已经成为过去式了。

Besides portability, Unix and C had some other important strengths. Both were constructed from a ``Keep It Simple, Stupid'' philosophy. A programmer could easily hold the entire logical structure of C in his head (unlike most other languages before or since) rather than needing to refer constantly to manuals; and Unix was structured as a flexible toolkit of simple programs designed to combine with each other in useful ways.
除了跨平台的优点外，Unix与C还有许多显著的优势。Unix与C的设计哲学是Keep It Simple, Stupid'。programmer可以轻易掌握整个C的逻辑结构（不像其他之前或以後的程式语言）而不用一天到晚翻手册写程式。 而Unix提供许多有用的小工具程式，经过适当的组合（写成Shell script或Perl script），可以发挥强大的威力。

The combination proved to be adaptable to a very wide range of computing tasks, including many completely unanticipated by the designers. It spread very rapidly within AT&T, in spite of the lack of any formal support program for it. By 1980 it had spread to a large number of university and research computing sites, and thousands of hackers considered it home.
C与Unix的应用范围之广，出乎原设计者之意料，很多领域的研究要用到电脑时，他们是最佳拍档。 尽管缺乏一个正式支援的机构，它们仍在AT&T内部中疯狂的散播。到了1980年，已蔓延到大学与研究机构，还有数以千计的hacker想把Unix装在家里的机器上。

The workhorse machines of the early Unix culture were the PDP-11 and its descendant, the VAX. But because of Unix's portability, it ran essentially unaltered on a wider range of machines than one could find on the entire ARPAnet. And nobody used assembler; C programs were readily portable among all these machines.
当时跑Unix的主力机器是PDP-11、VAX系列的机器。不过由於UNIX的高移植性，它几乎可安装在所有的电脑机型上。一旦新型机器上的UNIX安装好，把软件的C原始码抓来重新编译就一切OK了，谁还要用汇编语言来开发软件？ 

Unix even had its own networking, of sorts—UUCP: low-speed and unreliable, but cheap. Any two Unix machines could exchange point-to-point electronic mail over ordinary phone lines; this capability was built into the system, not an optional extra. In 1980 the first Usenet sites began exchanging broadcast news, forming a gigantic distributed bulletin board that would quickly grow bigger than ARPAnet. Unix sites began to form a network nation of their own around Usenet.
有一套专为UNIX设计的网络 --- UUCP：一种低速、不稳但很成本低廉的网络。 两台UNIX机器用条电话线连起来，就可以使用互传电子邮件。UUCP是内建在UNIX系统中的，不用另外安装。於是UNIX站台连成了专属的一套网络，形成其Hacker文化。在1980第一个USENET站台成立之後，组成了一个特大号的分散式布告栏系统，吸引而来的人数很快地超过了ARPANET。

A few Unix sites were on the ARPAnet themselves. The PDP-10 and Unix/Usenet cultures began to meet and mingle at the edges, but they didn't mix very well at first. The PDP-10 hackers tended to consider the Unix crowd a bunch of upstarts, using tools that looked ridiculously primitive when set against the baroque, lovely complexities of LISP and ITS. ``Stone knives and bearskins!'' they muttered.
少数UNIX站台有连上ARPANET。PDP-10与UNIX的Hacker文化开始交流， 不过一开始不怎么愉快就是了。PDP-10的Hacker们觉得UNIX的拥护者都是些什么也不懂的新手，比起他们那复杂华丽，令人爱不释手的LISP与ITS，C与 UNIX简直原始的令人好笑。『一群穿兽皮拿石斧的野蛮人』他们咕哝著。

And there was yet a third current flowing. The first personal computer had been marketed in 1975; Apple was founded in 1977, and advances came with almost unbelievable rapidity in the years that followed. The potential of microcomputers was clear, and attracted yet another generation of bright young hackers. Their language was BASIC, so primitive that PDP-10 partisans and Unix aficionados both considered it beneath contempt.
在这当时，又有另一股新潮流风行起来。第一部PC出现在1975年；苹果电脑在1977年成立，以飞快的速度成长。微电脑的潜力，立刻吸引了另一批年轻的 Hackers。他们最爱的程式语言是BASIC，由於它过於简陋，PDP-10 的死忠派与UNIX迷们根本不屑用它，更看不起使用它的人。

## 古老时代的终结

So matters stood in 1980; three cultures, overlapping at the edges but clustered around very different technologies. The ARPAnet/PDP-10 culture, wedded to LISP and MACRO and TOPS-10 and ITS and SAIL. The Unix and C crowd with their PDP-11s and VAXen and pokey telephone connections. And an anarchic horde of early microcomputer enthusiasts bent on taking computer power to the people.
1980年同时有三个Hacker文化在发展，尽管彼此偶有接触与交流，但还是各玩各的。ARPANET/PDP-10文化， 玩的是LISP、MACRO、TOPS-10与ITS。UNIX与C的拥护者用电话线把他们的PDP-11与VAX机器串起来玩。 还有另一群散乱无秩序的微电脑迷，致力於将电脑科技平民化。

Among these, the ITS culture could still claim pride of place. But stormclouds were gathering over the Lab. The PDP-10 technology ITS depended on was aging, and the Lab itself was split into factions by the first attempts to commercialize artificial intelligence. Some of the Lab's (and SAIL's and CMU's) best were lured away to high-paying jobs at startup companies.
三者中ITS文化（也就是以MIT AI LAB为中心的Hacker文化）可说在此时达到全盛时期， 但乌云逐渐笼罩这个实验室。ITS赖以维生的PDP-10逐渐过时，开始有人离开实验室去外面开公司，将人工智慧的科技商业化。MIT AI Lab 的高手挡不住新公司的高薪挖角而纷纷出走，SAIL与CMU也遭遇到同样的问题。

The death blow came in 1983, when DEC cancelled its `Jupiter' followon to the PDP-10 in order to concentrate on the PDP-11 and VAX lines. ITS no longer had a future. Because it wasn't portable, it was more effort than anyone could afford to move ITS to new hardware. The Berkeley variant of Unix running on a VAX became the hacking system par excellence, and anyone with an eye on the future could see that microcomputers were growing in power so rapidly that they were likely to sweep all before them.
致命一击终於来临，1983年DEC宣布：为了要集中在PDP-11与VAX生产线， 将停止生产PDP-10；ITS没搞头了，因为它无法移植到其他机器上，或说根本没人办的到。而Berkeley Univeristy修改过的UNIX在新型的VAX跑得很顺，是 ITS理想的取代品。有远见的人都看得出，在快速成长的微电脑科技下，Unix一统江湖是迟早的事。

It's around this time that Levy wrote Hackers. One of his prime informants was Richard M. Stallman (inventor of Emacs), a leading figure at the Lab and its most fanatical holdout against the commercialization of Lab technology.
差不多在此时Steven Levy完成``Hackers'' 这本书，主要的资料来源是Richard M. Stallman(RMS)的故事，他是MIT AI Lab领袖人物，坚决反对实验室的研 究成果商业化。

Stallman (who is usually known by his initials and login name, RMS) went on to form the Free Software Foundation and dedicate himself to producing high-quality free software. Levy eulogized him as ``the last true hacker'', a description which happily proved incorrect.
Stallman接著创办了Free Software Foundation，全力投入写出高品质的自由软件。Levy以哀悼的笔调描述他是the last true hacker'，还好事实证明Levy完全错了。

Stallman's grandest scheme neatly epitomized the transition hackerdom underwent in the early eighties—in 1982 he began the construction of an entire clone of Unix, written in C and available for free. His project was known as the GNU (Gnu's Not Unix) operating system, in a kind of recursive acronym. GNU quickly became a major focus for hacker activity. Thus, the spirit and tradition of ITS was preserved as an important part of the newer, Unix and VAX-centered hacker culture. Stallman's design finished what Berkeley had started, fusing the remains of the PDP-10 hacker culture with the Unix crowd.
Stallman的宏大计划可说是80年代早期Hacker文化的缩影 -- 在1982年他 开始建构一个与UNIX 相容但全新的操作系统，以C来写并完全免费。整个ITS的精神与传统，经由RMS的努力，被整合在一个新的，UNIX与VAX机器上的Hacker文化。 微电脑与区域网络的科技，开始对Hacker文化产生影响。Motorola 68000 CPU 加Ethernet是个有力的组合，也有几家公司相继成立生产第一代的工作站。 
Indeed, for more than a decade after its founding RMS's Free Software Foundation would largely define the public ideology of the hacker culture, and Stallman himself would be the only credible claimant to leadership of the tribe.

It was also around 1982–83 that microchip and local-area network technology began to have a serious impact on hackerdom. Ethernet and the Motorola 68000 microchip made a potentially potent combination, and several different startups had been formed to build the first generation of what we now call workstations.

In 1982, a group of Unix hackers from Stanford and Berkeley founded Sun Microsystems on the belief that Unix running on relatively inexpensive 68000-based hardware would prove a winning combination for a wide variety of applications. They were right, and their vision set the pattern for an entire industry. While still priced out of reach of most individuals, workstations were cheap for corporations and universities; networks of them (one to a user) rapidly replaced the older VAXes and other time-sharing systems.
1982年，一群Berkeley出来的UNIX Hacker成立了Sun Microsystems，他们的算盘打的是：把UNIX架在以68000为CPU的机器，物美价廉又符合多数应用程式的要求。他们的高瞻远嘱为整个工业界树立了新的里程碑。虽然对个人而言，工作站仍太昂贵，不过在公司与学校眼中，工作站真是比迷你电脑便宜太多了。在这些机构里，工作站（几乎是一人一台）很快地取代了老旧庞大的VAX等timesharing机器。

## 私有Unix时代

By 1984, when Ma Bell divested and Unix became a supported AT&T product for the first time, the most important fault line in hackerdom was between a relatively cohesive ``network nation'' centered around the Internet and Usenet (and mostly using minicomputer- or workstation-class machines running Unix), and a vast disconnected hinterland of microcomputer enthusiasts.
1984年AT&T解散了，UNIX正式成为一个商品。当时的Hacker文化分成两大类，一类集中在Internet与USENET上（主要是跑UNIX的迷你电脑或工作站连上网络），以及另一类PC迷，他们绝大多数没有连上Internet。

It was also around this time that serious cracking episodes were first covered in the mainstream press—and journalists began to misapply the term ``hacker'' to refer to computer vandals, an abuse which sadly continues to this day.

The workstation-class machines built by Sun and others opened up new worlds for hackers. They were built to do high-performance graphics and pass around shared data over a network. During the 1980s hackerdom was preoccupied by the software and tool-building challenges of getting the most use out of these features. Berkeley Unix developed built-in support for the ARPAnet protocols, which offered a solution to the networking problems associated with UUCP's slow point-to-point links and encouraged further growth of the Internet.
Sun与其他厂商制造的工作站为Hacker们开启了另一个美丽新世界。 工作站诉求的是高效能的绘图与网络，1980年代Hacker们致力为工作站撰写软件，不断挑战及突破以求将这些功能发挥到百分之一百零一。Berkeley发展出一套内建支援ARPANET protocols的UNIX，让UNIX能轻松连上网络，Internet也成长的更加迅速。

There were several attempts to tame workstation graphics. The one that prevailed was the X window system, developed at MIT with contributions from hundreds of individuals at dozens of companies. A critical factor in its success was that the X developers were willing to give the sources away for free in accordance with the hacker ethic, and able to distribute them over the Internet. X's victory over proprietary graphics systems (including one offered by Sun itself) was an important harbinger of changes which, a few years later, would profoundly affect Unix as a whole.
除了Berkeley让UNIX网络功能大幅提升外，尝试为工作站开发一套图形界面也不少。最有名的要算MIT开发的Xwindow了。Xwindow成功的关键在完全公开原始码，展现出Hacker一贯作风，并散播到Internet上。X 成功的干掉其他商业化的图形界面的例子，对数年後UNIX的发展有著深远的启发与影响。

There was a bit of factional spleen still vented occasionally in the ITS/Unix rivalry (mostly from the ex-ITSers' side). But the last ITS machine shut down for good in 1990; the zealots no longer had a place to stand and mostly assimilated to the Unix culture with various degrees of grumbling.
少数ITS死忠派仍在顽抗著，到1990年最後一台ITS也永远关机长眠了；那些死忠派在穷途末路下只有悻悻地投向UNIX的怀抱。

Within networked hackerdom itself, the big rivalry of the 1980s was between fans of Berkeley Unix and the AT&T versions. Occasionally you can still find copies of a poster from that period, showing a cartoony X-wing fighter out of the ``Star Wars'' movies streaking away from an exploding Death Star patterned on the AT&T logo. Berkeley hackers liked to see themselves as rebels against soulless corporate empires. AT&T Unix never caught up with BSD/Sun in the marketplace, but it won the standards wars. By 1990, AT&T and BSD versions were becoming harder to tell apart, having adopted many of each other's innovations.
UNIX们此时也分裂为BerkeleyUNIX与AT&T两大阵营，也许你看过一些当时的海报，上面画著一台钛翼战机全速飞离一个爆炸中、上面印著AT&T的商标的死星。Berkeley UNIX的拥护者自喻为冷酷无情的公司帝国的反抗军。 就销售量来说，AT&TUNIX始终赶不上BSD/Sun，但它赢了标准制订的战争。到1990年，AT&T与BSD版本已难明显区分，因为彼此都有采用对方的新发明。

After 1987, the workstation technology of the previous decade began to look distinctly threatened by newer, low-cost and high-performance personal computers based on the Intel 386 chip and its descendants. For the first time, individual hackers could afford to have home machines comparable in power and storage capacity to the minicomputers of ten years earlier—Unix engines capable of supporting a full development environment and talking to the Internet.
随著90年代的来到，工作站的地位逐渐受到新型廉价的高档PC的威胁，他们主要是用Intel80386系列CPU。第一次Hacker能买一台威力等同於十年前的迷你电脑的机器，上面跑著一个完整的UNIX，且能轻易的连上网络。

The MS-DOS world remained blissfully ignorant of all this. Though those early microcomputer enthusiasts quickly expanded to a population of DOS and Mac hackers orders an magnitude greater than that of the ``network nation'' culture, they never become a self-aware culture themselves. The pace of change was so fast that fifty different technical cultures grew and died as rapidly as mayflies, never achieving quite the stability necessary to develop a common tradition of jargon, folklore, and mythic history. The absence of a really pervasive network comparable to UUCP or Internet prevented them from becoming a network nation themselves.
沈浸在MS-DOS世界的井底蛙对这些巨变仍一无所知，从早期只有少数人对微电脑有兴趣，到此时玩DOS与Mac的人数已超过所谓的"网络民族"的文化，但他们始终没成什么气候或搞出什么飞机，虽然聊有佳作光芒乍现，却没有稳定发展出统一的文化传统，术语字典，传奇故事与神话般的历史。它们没有真正的网络，只能聚在小型的BBS 站或一些失败的网络如FIDONET。

Widespread access to commercial online services like CompuServe and GEnie was beginning to take hold, but the fact that non-Unix operating systems don't come bundled with development tools meant that very little source was passed over them. Thus, no tradition of collaborative hacking developed.
提供上网服务的公司如CompuServe或Genie生意日益兴隆，事实显示non-UNIX的操作系统因为并没有内附如compiler等程式发展工具，很少有source 在网络上流传，也因此无法形成合作开发软件的风气。 

The mainstream of hackerdom, (dis)organized around the Internet and by now largely identified with the Unix technical culture, didn't care about the commercial services. These hackers wanted better tools and more Internet, and cheap 32-bit PCs promised to put both in everyone's reach.
Hacker文化的主力，是散布在Internet各地，几乎可说是玩UNIX的文化。他们玩电脑才不在乎什么售後服务之类，他们要的是更好的工具、更多的上网时间、还有一台便宜32-bitPC。

But where was the software? Commercial Unixes remained expensive, in the multiple-kilobuck range. In the early 1990s several companies made a go at selling AT&T or BSD Unix ports for PC-class machines. Success was elusive, prices didn't come down much, and (worst of all) you didn't get modifiable and redistributable sources with your operating system. The traditional software-business model wasn't giving hackers what they wanted.
机器有了，可以上网了，但软件去哪找？商业的UNIX贵的要命，一套要好几千大洋($)。90年代早期， 开始有公司将AT&T与BSDUNIX移植到PC上出售。成功与否不论，价格并没有降下来，更要紧的是没有附原始码， 你根本不能也不准修改它，以符合自己的需要或拿去分享给别人。传统的商业软件并没有给Hacker们真正想要的。

Neither was the Free Software Foundation. The development of HURD, RMS's long-promised free Unix kernel for hackers, got stalled for years and failed to produce anything like a usable kernel until 1996 (though by 1990 FSF supplied almost all the other difficult parts of a Unix-like operating system).
即使是FreeSoftwareFoundation(FSF)也没有写出Hacker想要的操作系统，RMS承诺的GNU操作系统--HURD 说了好久了，到1996年都没看到影子(虽然1990年开始，FSF的软件已经可以在所有的UNIX平台执行)。

Worse, by the early 1990s it was becoming clear that ten years of effort to commercialize proprietary Unix was ending in failure. Unix's promise of cross-platform portability got lost in bickering among half a dozen proprietary Unix versions. The proprietary-Unix players proved so ponderous, so blind, and so inept at marketing that Microsoft was able to grab away a large part of their market with the shockingly inferior technology of its Windows operating system.

In early 1993, a hostile observer might have had grounds for thinking that the Unix story was almost played out, and with it the fortunes of the hacker tribe. And there was no shortage of hostile observers in the computer trade press, many of whom had been ritually predicting the imminent death of Unix at six-month intervals ever since the late 1970s.

In those days it was conventional wisdom that the era of individual techno-heroism was over, that the software industry and the nascent Internet would increasingly be dominated by colossi like Microsoft. The first generation of Unix hackers seemed to be getting old and tired (Berkeley's Computer Science Research group ran out of steam and would lose its funding in 1994). It was a depressing time.

Fortunately, there had been things going on out of sight of the trade press, and out of sight even of most hackers, that would produce startlingly positive developments in later 1993 and 1994. Eventually, these would take the hacker culture in a whole new direction and to undreamed-of successes.

## 早期的免费Unix

Into the gap left by the Free Software Foundation's uncompleted HURD had stepped a Helsinki University student named Linus Torvalds. In 1991 he began developing a free Unix kernel for 386 machines using the Free Software Foundation's toolkit. His initial, rapid success attracted many Internet hackers to help him develop Linux, a full-featured Unix with entirely free and re-distributable sources.
在这空窗期中，1992年一位芬兰HelsinkiUniversity的学生--LinusTorvalds开始在一台386PC上发展一个自由软件的UNIX kernel，使用FSF的程式开发工具。他很快的写好简单的版本，丢到网络上分享给大家，吸引了非常多的Hacker来帮忙一起发展Linux-一个功能完整的UNIX，完全免费且附上全部的原始码。 

Linux was not without competitors. In 1991, contemporaneously with Linus Torvalds's early experiments, William and Lynne Jolitz were experimentally porting the BSD Unix sources to the 386. Most observers comparing BSD technology with Linus's crude early efforts expected that BSD ports would become the most important free Unixes on the PC.

The most important feature of Linux, however, was not technical but sociological. Until the Linux development, everyone believed that any software as complex as an operating system had to be developed in a carefully coordinated way by a relatively small, tightly-knit group of people. This model was and still is typical of both commercial software and the great free-software cathedrals built by the Free Software Foundation in the 1980s; also of the freeBSD/netBSD/OpenBSD projects that spun off from the Jolitzes' original 386BSD port.
Linux最大的特色，不是功能上的先进而是全新的软件开发模式。直到Linux 的成功前，人人都认为像操作系统这么复杂的软件，非得要靠一个开发团队密切合作，互相协调与分工才有可能写的出来。商业软件公司与80年代的FreeSoftwareFoundation所采用都是这种发展模式。

Linux evolved in a completely different way. From nearly the beginning, it was rather casually hacked on by huge numbers of volunteers coordinating only through the Internet. Quality was maintained not by rigid standards or autocracy but by the naively simple strategy of releasing every week and getting feedback from hundreds of users within days, creating a sort of rapid Darwinian selection on the mutations introduced by developers. To the amazement of almost everyone, this worked quite well.
Linux则迥异於前者。一开始它就是一大群Hacker在网络上一起涂涂抹抹出来的。 没有严格品质控制与高层决策发展方针，靠的是每周发表新版供大家下载测试，测试者再把bug与patch贴到网络上改进下一版。一种全新的物竞天择、去芜存菁的快速发展模式。令大夥傻眼的是，东修西改出来的Linux，跑的顺极了。

By late 1993 Linux could compete on stability and reliability with many commercial Unixes, and hosted vastly more software. It was even beginning to attract ports of commercial applications software. One indirect effect of this development was to kill off most of the smaller proprietary Unix vendors—without developers and hackers to sell to, they folded. One of the few survivors, BSDI (Berkeley Systems Design, Incorporated), flourished by offering full sources with its BSD-based Unix and cultivating close ties with the hacker community.
1993年底，Linux发展趋於成熟稳定，能与商业的UNIX一分高下，渐渐有商业应用软件移植到Linux上。不过小型UNIX厂商也因为Linux的出现而关门大吉 -因为再没有人要买他们的东西。幸存者都是靠提供BSD为基础的UNIX 的完整原始码，有Hacker加入发展才能继续生存。

These developments were not much remarked on at the time even within the hacker culture, and not at all outside it. The hacker culture, defying repeated predictions of its demise, was just beginning to remake the commercial-software world in its own image. It would be five more years, however, before this trend became obvious.
Hacker文化，一次次被人预测即将毁灭，却在商业软件充斥的世界中，披荆斩棘，筚路蓝缕，开创出另一番自己的天地。

## 网络大爆炸时代

The early growth of Linux synergized with another phenomenon: the public discovery of the Internet. The early 1990s also saw the beginnings of a flourishing Internet-provider industry, selling connectivity to the public for a few dollars a month. Following the invention of the World Wide Web, the Internet's already rapid growth accelerated to a breakneck pace.
Linux能快速成长的来自令一个事实：Internet大受欢迎，90年代早期ISP如雨後春笋般的冒出来， World-WideWeb的出现，使得Internet成长的速度，快到有令人窒息的感觉。

By 1994, the year Berkeley's Unix development group formally shut down, several different free Unix versions (Linux and the descendants of 386BSD) served as the major focal points of hacking activity. Linux was being distributed commercially on CD-ROM and selling like hotcakes. By the end of 1995, major computer companies were beginning to take out glossy advertisements celebrating the Internet-friendliness of their software and hardware!
BSD专案在1994正式宣布结束，Hacker们用的主要是免费的UNIX(Linux与一些4.4BSD的衍生版本)。而 LinuxCD-ROM销路非常好(好到像卖煎饼般)。近几年来Hacker们主要活跃在Linux与Internet发展上。WorldWideWeb让 Internet成为世界最大的传输媒体，很多80年代与90年代早期的Hacker们现在都在经营ISP。

In the late 1990s the central activities of hackerdom became Linux development and the mainstreaming of the Internet. The World Wide Web has at last made the Internet into a mass medium, and many of the hackers of the 1980s and early 1990s launched Internet Service Providers selling or giving access to the masses.

The mainstreaming of the Internet even brought the hacker culture the beginnings of respectability and political clout. In 1994 and 1995 hacker activism scuppered the Clipper proposal which would have put strong encryption under government control. In 1996 hackers mobilized a broad coalition to defeat the misnamed ``Communications Decency Act'' and prevent censorship of the Internet.
Internet的盛行，Hacker文化受到重视并发挥其政治影响力。94、95年美国政府打算把一些较安全、难解的编码学加以监控，不容许外流与使用。这个称为Clipper proposal的专案引起了Hacker们的群起反对与强烈抗议而半途夭折。96年Hacker又发起了另一项抗议运动对付那取名不当的"Communications DecencyAct"，誓言维护 Internet上的言论自由。

With the CDA victory, we pass out of history into current events. We also pass into a period in which your historian (rather to his own surprise) became an actor rather than just an observer. This narrative will continue in Revenge of the Hackers.
电脑与Internet在21世纪将是大家不可或缺的生活用品，现代孩子在使用Internet科技迟早会接触到Hacker文化。它的故事传奇与哲学，将吸引更多人投入。未来对Hacker们是充满光明的。

## Bibliography

[Levy] Levy, Steven; Hackers, Anchor/Doubleday 1984, ISBN 0-385-19195-2.

[Raymond] Raymond, Eric S.; The New Hacker's Dictionary, MIT Press, 3rd edition 1996. ISBN ISBN 0-262-68092-0.

David E. Lundstrom gave us an anecdotal history of the ``Real Programmer'' era in A Few Good Men From UNIVAC, 1987, ISBN-0-262-62075-8.
