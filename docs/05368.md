# 三星手机上可能有间谍软件

> 原文：<https://hackaday.com/2020/01/09/spyware-discovered-on-all-samsung-phones/>

[编者按:关于这个“间谍软件”现在有一个持续的来回。我们还没有在任何手机上亲自研究过它，并且似乎缺乏清洁软件发送回家的解码 Wireshark caps 它可能是无害的。我们将原文保留如下，但在进一步的证据出现之前，你可能要对此持保留态度。或者在评论中让我们了解最新情况。但是不要急于下结论。]

如果你想要一部 Android 智能手机，三星可能有最高端的硬件选项，但这并没有阻止他们对有时装载的软件做出一些有问题的决定。通常这些手机都带有“默认”应用，无法通过普通手段删除，甚至无法禁用，而最新发现的与三星手机上预装软件相关的[似乎存在相当大的安全漏洞](https://www.reddit.com/r/Android/comments/ektg8u/chinese_spyware_preinstalled_on_all_samsung/)。

这个有问题的软件是手机“设备维护”部分的“存储清洁器”，它应该处理文件优化和删除。这个特殊的应用程序是由一家名为奇虎 360 的中国公司开发的，不使用亚行或 root 用户就无法从手机中删除。该公司因在病毒扫描方面极其糟糕的做法而闻名，该软件被指控将手机文件的所有信息发送到中国的服务器上，这些服务器可能会将它拥有的所有数据交给中国政府。这都是通过使用数据包捕获和 osint 发现的，这将在帖子中讨论。

这些爆料来自于最近在 Reddit 上发表最初声明的[kchaxcer]。在这一点上，这似乎也是相当合理的，另一个名为[GeorgePB]的用户能够在原始帖子的评论中提供一个[临时解决方案/变通办法](https://www.reddit.com/r/Android/comments/ektg8u/chinese_spyware_preinstalled_on_all_samsung/fddnlm0/)。这是一个有趣的问题，可能不应该存在于任何手机上，更不用说与各种 iphone 竞争的旗舰手机了，但它确实凸显了一些安全问题，当我们无法控制我们理应拥有的硬件上的软件时，我们都应该对日常使用的设备有所担忧。如果你是对开源手机感兴趣的 T2 人，还有一些选择。

感谢[kickaxe]的提示！

图片来自[庞卡基特【CC BY-SA 3.0 DE(https://creative commons . org/licenses/BY-SA/3.0/DE/deed . en)】](https://commons.wikimedia.org/wiki/File:Samsung_Galaxy_Note_5,_S6_edge%2B_and_Note_7_backside_20161010.jpg)