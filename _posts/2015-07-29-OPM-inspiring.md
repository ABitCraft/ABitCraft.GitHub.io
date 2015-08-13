---
layout: post
title: FireEye大牛解释联邦人事局事件的启示
---

对于 OPM（Office of Personnel Management，美国联邦人事局）数据窃取问题的媒体讨论以及相应的调查过程与听证会已经持续挺长时间了，我们先结合官方的报告稍微回顾一下这里都发生了那些事情：

> + 4月，OPM[发现](https://www.opm.gov/cybersecurity/)其存储的420万在职与离任联邦政府雇员人事信息遭窃。
> + 6月初，OPM在调查上述问题的过程中发现有更多信息被窃——背景调查数据库的[2150万](http://arstechnica.com/security/2015/07/call-it-a-data-rupture-hack-hitting-opm-affects-21-5-million/)（截至7月10日）在职、离任及潜在联邦雇员与合同工的个人信息。
> + 6月23日及6月24日，针对联邦人事局的[参议院听证会](http://arstechnica.com/information-technology/2015/06/opm-director-on-security-issues-were-trying-very-hard/)与国土安全部在事件中所负责任的[听证会](http://homeland.house.gov/hearing/subcommittee-hearing-dhs-efforts-secure-gov)分别举行。
> + 7月11日，在OPM公布被窃信息达到2150万人不到24小时，Katherine Archuleta局长[辞职](http://arstechnica.com/tech-policy/2015/07/opm-director-resigns-after-news-that-hack-affected-21-5-million-people/)。
> + 7月21日，奥巴马当局决定[不公开](https://www.washingtonpost.com/world/national-security/us-avoids-blaming-china-in-data-theft-seen-as-fair-game-in-espionage/2015/07/21/03779096-2eee-11e5-8353-1215475949f4_story.html)此次调查的证据。

在此期间，《网络安全监控实战》一书作者，FireEye首席安全战略官Richard Bejtlich通过其个人博客TaoSecurity持续跟进此事，不断澄清媒体及外行人对于国土安全部的网络安全防护项目的错误理解。国土安全部被媒体热议的安全项目有两个：CDM（[Continuous Diagnostics and Mitigation](https://www.us-cert.gov/cdm)，持续诊断监控项目负责搜寻内部系统缺陷）和 E3A（[EINSTEIN 3 Accelerated](http://www.dhs.gov/publication/einstein-3-accelerated)，负责监控恶意流量，是价值45亿美元的国家网络安全与防护项目的核心能力）。

<img src="{{ site.baseurl }}/images/cdm-process.jpg"  alt="CDM Process" />

Richard Bejtlich在第一篇文章[Continuous Diagnostic Monitoring Does Not Detect Hackers](http://taosecurity.blogspot.com/2015/06/continuous-diagnostic-monitoring-does.html)中纠正了The Hill网站编辑[Cory Bennett](http://thehill.com/policy/cybersecurity/244365-federal-cyber-protection-knocked-as-outdated-behind-schedule)的错误理解。如上图所示，CDM项目的作用只是查找内部系统缺陷，最后还需由技术人员来修补漏洞。第二篇文章[Hearing Witness Doesn't Understand CDM](http://taosecurity.blogspot.com/2015/06/hearing-witness-doesnt-understand-cdm.html)反驳的是前国土安全部官员Daniel M. Gerstein在听证会上对于CDM的错误解读，CDM所处理的只是内部系统漏洞，如果这些漏洞得不到修补的话就会成为潜在的恶意风险，这些漏洞本身并非恶意行为，恶意行为是入侵者攻击所致。简而言之，CDM有助于降低恶意风险，但并不能识别甚至阻止恶意行为，这一项目只不过是为了更快地找出并修复系统漏洞。

<img src="{{ site.baseurl }}/images/E3A-works.jpg"  alt="EINSTEIN 3 Accelerated Works" />

Ars Technica编辑、前海军军官Sean Gallagher的文章[Why the “biggest government hack ever” got past the feds](http://arstechnica.com/security/2015/06/why-the-biggest-government-hack-ever-got-past-opm-dhs-and-nsa/)则专门分析了E3A系统的来龙去脉。如上图所示，E3A系统部署于网关处，原本是基于深度包检测技术，最近一次价值2.18亿美元的功能升级让它具备了恶意流量分析及签名检测能力，不过它仍需国土安全部的技术人员来告诉它具体去分析或检测什么。根据已经发生过的攻击方式的特征，E3A有能力阻止它们再次发生；但是在面对尚未发现的“0-Day”及其伪装成正常流量的全新攻击方式时，E3A的上述功能就无能为力了。

考虑到当前的安全系统的功能，那么尚未发生的攻击行为基本都会以某种全新的方式进行，而任何系统都不可能做到阻绝入侵者去发掘新的攻击方式。Richard Bejtlich在第三篇文章[My Security Strategy: The "Third Way”](http://taosecurity.blogspot.com/2015/06/my-security-strategy-third-way.html)中提出用“检测与响应”策略来加以应对。因为在他看来，入侵与破坏还是有一些区别的，事实上你可以承受住非授权的登陆，但登陆之后的窃密与破坏就大不相同了。在没有任何网络是绝对安全的今天，最有效的安全策略只能是首先尽可能多地阻止入侵行为，同时以“检测与响应”机制来避免或是最小化那些未能阻止的入侵行为可能造成的破坏。

Ryan G. 在“The Third Way”这篇文章的评论中说道，“我想把这打印出来并放到我的CISO办公桌上一份。”
