---
layout: post

title: 【翻译】GitHub 遭到 DDoS 攻击
---
*这里是一篇试译，原文是 Alex Armstrong 于2015年3月30日发表于 [I Programmer](http://www.i-programmer.info) 的 [GitHub Under DDoS Attack](http://www.i-programmer.info/news/149-security/8440-github-under-ddos-attack-.html) .*

***

GitHub 遭受到其历史上最大规模的拒绝式服务（DDoS）攻击。攻击流量针对的是其两个涉及到中国人权问题和互联网接入自由的网址。

GitHub 已经被 DDoS 攻击好几天了。攻击开始于上周四，3月26日 UTC 时间（世界标准时间）凌晨2点，虽偶有波动但攻击一直在持续着。GitHub 看起来还能应付，目前还没有用户无法访问代码仓库或其他内容的报告。

这次攻击的性质是不同的，一个新的手法就是利用几乎所有访问中国网站的无辜用户来进行攻击。根据 Insight-labs 的博客，是位于中国国内网络和国际互联网交界处的设备劫持了所有通过百度统计服务的 HTTP 连接，并把原来的 Javascript 代码替换成了每2秒加载一次 https://github.com/greatfire/ 和 https://github.com/cn-nytimes/ 地址的功能。这意味着任何使用百度统计服务访问中国网站的用户都在参与这次攻击。

受影响的网址首先是 GreatFire 的 GitHub 页面，一个反对中国审查制度的组织——这个名字为的是针对限制国际互联网访问权限的“中国防火长城”工程。

其次是一个提供《纽约时报》网站镜像地址的页面，这样《纽约时报》的内容就可以通过防火长城。

这里怀疑此次攻击是由中国当局组织的，因其最近刚被 GreatFire 批评过。

GitHub 官方博客仅仅说道：

> " Based on reports we've received, we believe the intent of this attack is to convince us to remove a specific class of content."
>
> （“基于我们收到的报告，我们相信这次攻击的目的是想说服我们去移除一类具体的内容。”）

如果你发现你对 GitHub 的访问变慢了，那么现在你就知道原因在哪里了。

访问 [GitHub status site](https://status.github.com/) 可以了解正在发生的事情。

***

参考文章：

+ Solidot: [对GitHub的大规模DDoS攻击已超过80个小时](http://www.solidot.org/story?sid=43506)
+ 新浪科技：[持续80多小时：GitHub遭大规模DDoS攻击](http://tech.sina.com.cn/s/2015-03-31/074110022397.shtml)
+ NETRESEC: [China's Man-on-the-Side Attack on GitHub](http://www.netresec.com/?page=Blog&month=2015-03&post=China%27s-Man-on-the-Side-Attack-on-GitHub)
+ Hacker News: [China's Man-On-the-Side Attack on GitHub (netresec.com)](https://news.ycombinator.com/item?id=9293849)
+ Solidot: [中国对GitHub发动的是Man-on-the-side攻击](http://www.solidot.org/story?sid=43530)
