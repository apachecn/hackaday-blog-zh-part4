# 本周安全:地缘政治黑客行动主义、反病毒挖掘和 Linux 恶意软件

> 原文：<https://hackaday.com/2022/01/28/this-week-in-security-geopolitical-hacktivism-antivirus-mining-and-linux-malware/>

~~中情局~~黑客行动主义者发起了[一场针对白俄罗斯铁路系统](https://arstechnica.com/information-technology/2022/01/hactivists-say-they-hacked-belarus-rail-system-to-stop-russian-military-buildup/)的勒索活动，但他们想要的不是加密货币，而是释放政治犯和驱逐俄罗斯士兵。这可以被称为网络恐怖主义的一个例子，尽管有一个合理的理论认为这是一个国家支持的黑客行为，伪装成黑客行动主义。似乎可以确定的是，有东西中断了铁路运输，推特上的一个小组[提供了令人信服的违规证据](https://twitter.com/cpartisans/status/1486090490655252481)。

## 您的防病毒软件现在包括了一个密码挖掘器

现在不要看，但你最新更新的[诺顿 360](https://krebsonsecurity.com/2022/01/norton-360-now-comes-with-a-cryptominer/) 或[阿维拉](https://krebsonsecurity.com/2022/01/500m-avira-antivirus-users-introduced-to-cryptomining/)可能安装了加密货币挖掘模块。令人欣慰的是，还保留了一些理智，并且在您的机器开始将空闲周期用于挖掘之前，您必须选择加入加密方案。对于这样做的用户，他们被放入一个采矿池，为大多数硬件支付小额费用。诺顿自然会从他们的麻烦中抽取 15%的费用。

## Linux 恶意软件的状态

以前有句格言说 Linux 机器不会有恶意软件。这从来都不是真的，但是对服务器领域的持续征服产生了副作用，使得 Linux 恶意软件变得更加危险。2021 年，Crowdstrike 发现 Linux 恶意软件增加了 35%,其中三个不同的类别居首:XorDDoS、Mozi 和 Mirai 未来组合。

## pankit

说到 Linux，一个相当严重的 [Linux 漏洞刚刚被公布](https://www.qualys.com/2022/01/25/cve-2021-4034/pwnkit.txt)，并且[一个工作漏洞已经被释放](https://haxx.in/files/blasty-vs-pkexec2.c)。这个问题是`Polkit`二进制中的一个简单问题，出于这个目的，它可以被认为是一个`sudo`选择。重要的是，它是一个 setuid 二进制文件，当由非特权用户执行时，它会将自己的特权提升到 root。“等等，”我听到你说，“这听起来像是一个可怕的安全问题！”有可能，当它出错的时候。但简单的事实是，有时用户需要执行一个原本需要 root 权限的操作。一个简单的例子，`ping`，需要打开一个原始的网络套接字才能运行。这些二进制文件被精心设计为只允许有限的操作，但有时一个 bug 允许逃离这个“沙箱”。

那么`pkexec`有什么故事？NULL `argv`。好了，Linux 编程 101 次。当一个程序在 Linux 上启动时，它会被传递两个参数，通常命名为`argc`和`argv`。它们分别是一个整数和一个字符指针数组。如果你不是程序员，那就把它想象成参数的数量，以及参数的列表。这些信息用于解析和处理程序中的命令行选项。`argc`始终至少是一个，而`argv[0]`将始终包含被执行的二进制文件的名称。只不过，情况并不总是这样。还有另一种启动二进制文件的方法，使用`execve()`函数。该函数允许程序员直接指定参数列表，包括参数 0。

如果这个列表是空的，会发生什么呢？如果编写一个程序来考虑这种可能性，就像`sudo`，那么一切都很好。然而，`pkexec`不包括对空的`argv`或为 0 的`argc`的检查。它的行为就像有一个参数要读取，程序初始化在内存中发生的方式，它实际上访问的是第一个环境变量，并将其视为一个参数。它检查系统路径中匹配的二进制文件，并重写它认为是它的参数列表，但实际上是环境变量。这意味着不受控制的文本可以作为环境变量注入到 setuid 程序`pkexec`中。

这很有意思，但不是立即有用，因为`pkexec`在注入发生后很快就清除了它的环境变量。那么我们可以用什么鬼祟的技巧来真正利用这一点呢？抛出错误信息。`pkexec`将使用`gconv`共享库打印一条错误消息，它从寻找`gconv-modules`配置文件开始。该文件定义了要打开的特定库文件。环境变量`GCONV_PATH`可以用来指定一个替代的配置文件，但是这个环境变量在运行 setuid 二进制文件时被阻塞了。啊，但是我们有办法在这种情况发生后注入一个环境变量。这就是剥削。准备一个包含我们任意代码的`payload.so`，一个指向有效负载的假`gconv-modules`文件，然后使用 NULL argv 技巧注入`GCONV_PATH`环境变量。Whoami？根。

这个故事有几个有趣的转折。首先，[【瑞安·马龙】在 2013 年痛苦地接近发现这个漏洞](https://ryiron.wordpress.com/2013/12/16/argv-silliness/)。其次，早在 2007 年，[【Michael Kerrisk】就报告了 NULL `argv`怪癖是一个 Linux 内核错误](https://bugzilla.kernel.org/show_bug.cgi?id=8408)。

## 攻击随机密码

最安全的密码是随机生成的，对吗？是的，但是如果随机发生器并不像看起来那样随机呢？现在，我们这次不是在讨论有意的后门，而是看似[无关紧要的模式，它们有时会产生很大的影响](https://www.trustedsec.com/blog/recovering-randomly-generated-passwords/)。毕竟，恩尼格玛机被破解的部分原因是它永远不会把一个字母编码成它自己。TrustedSec 的 Hans Lakhan 研究了 LastPass 生成的一百万个密码，并试图从数据中归纳出一些有用的东西。大多数密码都是 1 位或 2 位数字。注意这不是算法的弱点，只是可用字符的预期结果。强制密码使用每个猜测必须包含一个或两个数字的规则是否有优势？这肯定会减少攻击空间，但也会遗漏不符合该模式的密码。这种交换值得吗？

答案并不明确。在某些情况下，使用建议的规则会有一点好处。但是随着暴力过程的继续，这种优势消失了。不管怎样，这都是一次将统计学应用于密码破解的迷人尝试。

## WordPress 和后门主题

WordPress 主题和插件的较大生产商之一，AccessPress，遭遇了一次网站漏洞，情况变得很糟糕。这个问题是由 Jetpack 的研究人员发现的，他们正在对不同的受损网站进行事后分析，并且[发现了嵌入在 AccessPress 主题](https://jetpack.com/2022/01/18/backdoor-found-in-themes-and-plugins-from-accesspress-themes/)中的恶意软件。第一次违规发生在 2021 年 9 月，因此，如果在 2021 年 9 月至 10 月中旬之间下载，请怀疑 AccessPress 的任何内容。注意，如果从 WordPress.org 目录安装，这些主题是安全的。已知的受感染插件和主题列表可在上面的链接中找到，以及其他危害的指标。

## 比特和字节

还有另一个秘密令牌在源代码中被意外泄露，即 Twitter 访问令牌。Github 已经自动扫描存储库中意外包含的凭证，但这不包括 Twitter 令牌。【隐姓埋名】写了一个快速扫描器，[找到了大约 9500 个](https://incognitatech.medium.com/using-twitter-to-notify-careless-developers-the-unorthodox-way-d71478ad367a)有效代币。(此处插入超过 9000 个迷因。)问题怎么通知这么多人？创建一个 bot，发布一条 tweet，然后使用令牌进行转发。这肯定会引起一些关注。

> 如果你不记得转发了这条消息，这意味着你已经在一个公共的 GitHub 存储库中泄露了你的 Twitter 访问令牌。不是最佳实践，对吧？
> 详情请阅读我们的最新文章:[https://t.co/6WBC6DRNDS](https://t.co/6WBC6DRNDS)#信息安全 #网络安全 # GitHub
> 
> — PinataHub_Bot (@PinataHub_Bot) [January 24, 2022](https://twitter.com/PinataHub_Bot/status/1485647404695265284?ref_src=twsrc%5Etfw)