# 本周安全:出血的牙齿，坏邻居，和无法撬开的锁

> 原文：<https://hackaday.com/2020/10/16/this-week-in-security-bleedingtooth-bad-neighbors-and-unpickable-locks/>

本周,《爆牙》的第一个细节泄露到了推特上,《T1 》,让《T2》有点疯狂。完整的细节尚未公布，但我们所知道的已经足够了。首先，BleedingTooth 不是一个单一的漏洞，而是一组至少 3 个不同的 CVE(这难道不应该使它 bleeding tooth？).到目前为止，最严重的漏洞是 CVE-2020-12351，这似乎是在休息后嵌入的视频中展示的。

 [https://www.youtube.com/embed/qPYrLRausSw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/qPYrLRausSw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



我们确实对此有所了解，以谷歌安全顾问的形式。包括一个概念证明，它会在目标机器上触发内核崩溃。不清楚目标机是需要先配对，还是蓝牙开机就够了。核心问题是恶意的蓝牙数据包可能会沿着非预期的代码路径前进，从而导致数据类型混淆。在问题解决之前，最好关闭笔记本电脑上的蓝牙。

### RFC6106 和坏邻居

本周是补丁星期二，有一个特别的 bug 引起了我的注意。CVE-2020-16898 是[如何处理 RFC6106 IPv6 路由广告的问题](https://www.mcafee.com/blogs/other-blogs/mcafee-labs/cve-2020-16898-bad-neighbor/)。正确格式化的数据包包含长度字段，该字段被定义为总是具有奇数值。当数据包的格式错误为偶数时，就会触发缓冲区溢出。

[概念验证代码可用](https://github.com/advanced-threat-research/CVE-2020-16898)。运行 PoC 会在未打补丁的机器上导致 BSoD。微软已经得出结论，由于 Windows 内核中现有的强化措施，将该缺陷转化为真正的代码执行漏洞将非常困难。此外，RFC6106 数据包仅用于本地网络，会被网关和 ISP 设备阻止。该漏洞不太可能被用于互联网攻击。

### 一把无法打开的挂锁？

开锁是一项令人着迷的实践。通过对锁的核心施加张力，单个的插销可以被提升到垂直线上，一旦它们都就位，锁就被撬开了。制造商一直试图让锁对撬锁和其他绕过方法更有弹性，但这种锁真正将这种努力推向了一个新的水平。下面的视频是 [BosnianBill](https://www.youtube.com/channel/UCp1orOGJwZvjLAvckyxC4Nw) 对这把无法撬开的锁的拆卸和分析。

 [https://www.youtube.com/embed/lPhAhAPtlH4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/lPhAhAPtlH4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



这里有几个奇怪的因素。首先，这不是一个主要的安全或制锁品牌，这是一个“盛刚”锁。这很可能是马跃设计的一系列锁的仿制品。除此之外，这种设计非常巧妙，在锁定机制中内置了一系列“气隙”。没有办法直接拉紧锁，唯一的拉力由内部弹簧提供。这种锁的设计是否真的无法撬开，或者是否最终会发现一个弱点，还有待观察。不管怎样，这个设计令人印象深刻，高安全性锁的未来似乎很有趣。

### 窥探智能手表

如果你有一个 Xplora 4 儿童智能手表，你可能想让它退役，因为助记实验室的研究人员发现了似乎是设备中的一个故意后门[。一旦收到加密签名的文本信息，这种基于 Android 的设备可以录制音频，拍照，并报告其位置。当一个技术硬件带有这样奇怪的功能时，它通常是调试那些从未被删除的功能。这种情况略有不同，因为智能手表是由奇虎 360 开发的，而奇虎 360 已经被列入美国国家安全威胁名单](https://www.mnemonic.no/blog/exposing-backdoor-consumer-products)。更不用说，当收集音频的功能被字面上标记为`wiretap`时，很难假设它没有恶意。

[通过寄存器](https://www.theregister.com/2020/10/12/xplora_4_smartwatches/)。

### 捉弄 Trickbot

[布莱恩·克雷布斯]在月初第一次注意到 Trickbot 僵尸网络的一些不寻常之处。他报告了发送给一些 Trickbot 实例的一组新指令，将命令和控制服务器设置为 localhost。虽然这不会删除感染，但可以防止受感染的机器采取进一步的定向操作。当时还有一些其他的伎俩，比如向控制服务器发送虚假的感染数据。这看起来像是对恶意软件网络的复杂攻击。

几天后，微软发布了一份声明，详细描述了他们削弱 Trickbot 网络的行动。这一时机立即表明[Krebs]正在报道微软的行动。虽然这是可能的，但微软报告中的细节并不完全一致。微软声称已经在 10 月 12 日采取了行动，而[Krebs]在 10 月 2 日已经观察了几天奇怪的行为。缓解步骤听起来也很不一样。尚不清楚这是否是针对 Trickbot 的两起独立行动。不管怎样，看到针对僵尸网络的具体行动总是好的。

### 黑苹果

我们已经报道了很多关于苹果设备漏洞的新闻，但是这个故事是关于[那些入侵苹果基础设施](https://samcurry.net/hacking-apple/)的家伙。整个故事是详细的，并且是进行这样的安全审计的有用指南。他们确定了基础设施，并开始寻找尚未更新的已知漏洞。总之，他们在苹果的基础设施中发现了 54 个独立的漏洞。它们包括 iCloud 中有趣的电子邮件蠕虫，由跨站点脚本攻击驱动，以及允许他们以管理员身份访问苹果官方论坛的智能安全旁路。这不是轻松的阅读，但如果你真的想知道红队如何对公共基础设施进行测试的细节，这是一个好的开始。