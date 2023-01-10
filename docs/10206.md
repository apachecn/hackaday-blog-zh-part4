# 本周安全:水坑攻击，勒索软件诡计，和更多管道新闻

> 原文：<https://hackaday.com/2021/05/21/this-week-in-security-watering-hole-attackception-ransomware-trick-and-more-pipeline-news/>

在可能是第一次的水坑攻击中，我们现在已经看到了[针对水坑](https://arstechnica.com/gadgets/2021/05/florida-water-plant-compromise-came-hours-after-worker-visited-malicious-site/)或至少供水设施的攻击。这一发现的方式有点奇怪——这是德拉戈在[调查佛罗里达州奥尔德斯马尔二月事件时发现的。一个专门从事水处理的佛罗里达承包商运营着一个 WordPress 站点，该站点托管了一个数据收集脚本。就在 Oldsmar 设施被攻破的当天，有人从那个地方访问了被攻破的网站。](https://www.dragos.com/blog/industry-news/a-new-water-watering-hole/)

你可能会像调查人员一样，立即想到对该网站的访问一定与 Oldsmar 处理厂的妥协有关。时间太可疑了，不可能是巧合，对吗？这就是问题所在，被入侵的网站只是在收集浏览器指纹，似乎后来被用来伪装僵尸网络。攻击本身很可能是通过 Teamviewer 进行的。我会注意到[这个故事的主要来源](https://us-cert.cisa.gov/sites/default/files/publications/AA21-042A_Joint_Cybersecurity_Advisory_Compromise_of_U.S._Drinking_Treatment_Facility.pdf)提到了 Teamviewer，但称之为未经证实。假设入侵确实发生在该平台上，那么网站访问不太可能是一个因素，这就是 Dragos 的结论。另一方面，很容易想象这样一种场景，其中记录的访问 IP 地址导致端口扫描，并发现 VNC 或远程桌面端口处于打开状态。

## 一个奇怪的勒索技巧

这次不是点击诱饵，我们保证。这个[确实是一个奇怪的把戏](https://krebsonsecurity.com/2021/05/try-this-one-weird-trick-russian-hackers-hate/)，它确实可以防止一些勒索病毒感染。要怪就怪[Brian Krebs]的 clickbait 标题，因为他让这种古怪广为人知。

相当大一部分勒索软件活动是在俄罗斯以外进行的，包括 DarkSide 对 Colonial Pipeline 的攻击。从历史上看，俄罗斯官员对俄罗斯国民犯下的计算机犯罪多少有些放任，只要受害者不是俄罗斯人或来自盟国。(虽然有相关的消息，但我们稍后会介绍。)一个俄罗斯罪犯是如何查到他们潜在的受害者住在哪里的？一种方法是检查机器上安装的语言，作为勒索软件安装的一部分。诀窍是什么？安装俄语和西里尔文虚拟键盘。无论如何，这都不是一个有保证的解决方案，但它可能会让你远离麻烦，而且不会有伤害。

## QNAP

对于 QNAP 和他们的用户，我们有更多的坏消息。首先，[刚刚公布了一对新的漏洞](https://www.shielder.it/advisories/qnap-musicstation-malwareremover-pre-auth-remote-code-execution/)，一个在 MusicStation 应用程序中，另一个具有讽刺意味的是，在 MalwareRemover 应用程序中。最初的报告是在去年的九月，修正版本在 5 月 6 日或之前发布。

其次，[q locker 勒索软件战役已经被拿下](https://www.bleepingcomputer.com/news/security/qlocker-ransomware-shuts-down-after-extorting-hundreds-of-qnap-users/)。这听起来像是一件好事，但随着活动的结束，支付解密密钥的机会也将结束。到目前为止，还没有一个解密程序发布，这看起来像是解密赎金数据的最后一步，直到有人可以破解它。

## 管道

关于殖民管道的新闻不断传来，其中一些是上周谣传的。首先，已经确认[是公司网络受到勒索软件](https://www.cnn.com/2021/05/12/politics/colonial-pipeline-ransomware-payment/index.html#:~:text=The%20company%20halted%20operations%20because%20its%20billing%20system%20was%20compromised,)的攻击，而不是管道运营本身。我知道很多人对这次停电实际上是由计费系统瘫痪引起的消息感到非常沮丧。在你拿出你的干草叉之前，记住一个破产的公司也不会把汽油泵入管道。

好消息是，[黑暗面似乎被解散了](https://krebsonsecurity.com/2021/05/darkside-ransomware-gang-quits-after-servers-bitcoin-stash-seized/)，他们的一些账户被查封了，至少他们的一些比特币被取走了，很可能是被执法部门取走了。换句话说，管道袭击达到了政治临界质量，并引发了连锁反应，导致执法行动，甚至可能是俄罗斯当局采取的行动。先不说细节，听起来解密工具就要发布了，这个特定的勒索病毒团伙就这么完了。

## 国际保险公司和勒索软件

大型国际保险公司之一的安盛保险公司(AXA)在上周末遭遇了三重威胁勒索病毒攻击。似乎不是整个公司，但亚洲的几个办公室受到了影响。妥协之后，他们的网站遭到了协同的 DDoS 攻击。攻击最糟糕的部分是数据，其中一些非常私人，除了被加密之外还被泄露。这包括医疗报告和合法身份证明文件。具有讽刺意味的是，安盛一周前刚刚宣布了一项新政策，即他们的法国保单将不再报销赎金。