# 本周安全:BYOVD、Spectre Vx、更多八进制头痛和 ExifTool

> 原文：<https://hackaday.com/2021/05/07/this-week-in-security-byovd-spectre-vx-more-octal-headaches-and-exiftool/>

在阅读关于戴尔 BIOS 更新系统中的一系列缺陷[时，我学到了一个新的缩写。因为戴尔已经修补了他们的驱动程序，但尚未撤销以前驱动程序版本的签名密钥，所以它容易受到 BYOVD 攻击。](https://labs.sentinelone.com/cve-2021-21551-hundreds-of-millions-of-dell-computers-at-risk-due-to-multiple-bios-driver-privilege-escalation-flaws/)

自带易受攻击的驱动程序是一种有趣的 Windows 权限提升方法。64 位版本的 Windows 有一个安全特性，可以阻止内核中未签名的内核驱动程序。该漏洞是将仍然具有有效签名的旧的已知易受攻击的驱动程序加载到内核中，并使用旧的漏洞来利用系统。需要注意的是，即使驱动程序已经签名，仍然需要一个管理员帐户来加载驱动程序。那么，当 BYOVD 攻击需要管理权限来完成时，它有什么用呢？

SentinelLabs 持有他们的概念证明，但我们可以推测。特定的易受攻击的驱动程序模块位于文件系统中的`C:\Windows\Temp`位置，该位置可由任何进程写入。可能的攻击是覆盖文件系统上的驱动程序，然后触发重新启动以加载旧的易受攻击的版本。如果您的戴尔电脑上仍在运行 Windows，那么一定要解决这个问题。

## 又一个幽灵缺陷

[Spectre 投机执行漏洞，又来袭](https://arstechnica.com/gadgets/2021/05/new-spectre-attack-once-again-sends-intel-and-amd-scrambling-for-a-fix/)。以前的版本通过缓存内存泄漏数据，而这次迭代通过微操作缓存泄漏内存。我经常开玩笑说，x86 处理器并没有真正运行 x86 指令集，它们只是模仿它。这部分是正确的，因为执行管道的一部分是将 x86 宏操作翻译成处理器特定的“类似 RISC 的微操作”。这个翻译过程有可能是一个复杂的操作，所以现代处理器有一个缓存来避免重复指令的重复过程。

弗吉尼亚大学和加州大学圣地亚哥分校的研究人员发表了他们关于这项技术的论文。对于这种新技术的严重性存在一些分歧，研究人员声称他们可以绕过当前所有内置的 Spectre 保护。英特尔已经声明，新技术不会绕过他们现有的缓解措施，AMD 尚未就该论文发表声明。时间会告诉我们实际上需要做多少工作来减轻投机性执行的另一个问题。

## Android 更新

本月的安卓安全补丁带来了三个严重的漏洞。 [CVE-2021-0473](https://android.googlesource.com/platform/system/nfc/+/cd0f77f71ff4166529fc22aa7db6c32dbb1d2c1c) 是 Android 系统如何处理 NFC 标签的一系列问题。无效的 NFC 消息可能导致双重释放、缓冲区溢出和内存泄漏。主要的解决方案似乎只是丢弃看起来无效的 NFC 数据包，而不是尝试处理它们。

[CVE-2021-0474](https://android.googlesource.com/platform/system/bt/+/2cafe07d66bfc5cc75d7d2bf61415fc33d711132) 和 [CVE-2021-0475](https://android.googlesource.com/platform/system/bt/+/a632a66b81ee4b1db65d0cf64b4ce525f56214ff) 都是蓝牙处理的问题。这两个都很简单。首先是一个容易犯的编码错误:使用`sizeof(p_pkt->len)`检查数据包的长度。`len`成员的大小是固定的——他们真的只想读取值。第二个蓝牙 bug 是一对缺失的`return`语句，当遇到某些错误条件时，会导致释放后使用。

## 更暧昧的 IP

八进制格式的 IP 地址似乎是[不断送给](https://sick.codes/sick-2021-014/)的礼物，这次是 Python `ipaddress`库。就在两年前，这个 Python3 库被修改为允许在 IP 地址中以“0”开头。正如我们之前所提到的，这会导致应用程序不同层之间的混淆，安全检查可能会允许某个地址在被执行时被理解为不同的地址。Python 开发人员采用了我认为正确的解决方案:[使所有以“0”开头的 IP 地址无效](https://github.com/python/cpython/pull/25099)。八进制地址格式从来都不符合 RFC，无论如何都应该避免。我们可能会多次回到这个故事，因为有人告诉我，其他几种语言和库也有完全相同的问题。

## 关闭安全系统

这是一个我们通常会一笑置之的比喻，当极客助手侵入一所房子的安全系统，从远处禁用它。但是，显然在 ABUS Secvest 系统的情况下，[真的很容易](https://eye.security/nl/blog/breaking-abus-secvest-internet-connected-alarm-systems-cve-2020-28973)。

Secvest 系统需要将端口 4433 转发到系统，以便从互联网对其进行管理。[Niels Teusink]指出这是一个优势，因为该系统可以在不依赖云系统的情况下进行远程管理。不利的一面是，这种 HTTPS 接口特别容易损坏。无需身份验证即可访问系统上的多个端点，包括一个转储系统配置的端点。包括在配置数据中吗？控制系统所需的明文用户 pin。

还有一个值得一看的技巧，许多系统都配置了动态 DNS。更新凭据也在配置数据中，因此攻击者不仅可以禁用系统，还可以接管动态 DNS 名称，每当所有者试图远程打开他们的摄像机时，就播放一段不感兴趣的视频。这是一个值得一个糟糕的好莱坞大片的黑客。

## 21 进出口电子邮件中的邮件

Exim 邮件服务器开始于 1995 年，作为 Unix 机器的邮件传输代理。Qualys 审计了 Exim，结果不太好。Qualys 将结果称为 21Nails，因为在这项工作中发现了 21 个严重的漏洞，其中许多漏洞可以追溯到该项目的 git 历史。虽然该报告不包括 PoC 代码，但它们可能会很快独立开发出来，所以如果你运行 Exim，现在就去更新你的服务器吧。

## ExifTool

最后，我们在 ExifTool 中有一个大问题:

> 任何使用 ExifTool 的人请确保更新到 12.24+版本，因为 CVE-2021-22204 可以被完全有效的图像(jpg，tiff，mp4 等等)触发，从而导致任意代码执行！[pic.twitter.com/VDoybw07f5](https://t.co/VDoybw07f5)
> 
> —威廉·鲍林(@ wcbowling)[2021 年 4 月 24 日](https://twitter.com/wcbowling/status/1385803927321415687?ref_src=twsrc%5Etfw)