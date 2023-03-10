# 单个固态硬盘从 System 7 到 High Sierra 的旅程

> 原文：<https://hackaday.com/2021/07/26/a-single-ssds-journey-from-system-7-to-high-sierra/>

有了一些空闲时间和一系列旧的苹果电脑，[Pierre Dandumont]想知道他是否可以不断地将单个操作系统驱动器从他最老的系统(Performa 630 上的 System 7.1)升级到 MacBook Air 上的最新版本的 MacOS。他回忆起看过一个演示从 DOS 到 Windows 10 持续升级的旧视频(我们认为【2016 年的这个视频可能就是这个)，这给了他这次旅程的灵感。[Pierre]在[的博客](https://www.journaldulapin.com/2021/07/19/upgrade-system-7-macos-12/)上记录了他的努力(法语；这里的英文翻译链接是。

一路走来，他安装了 24 种不同的操作系统

*   系统 7.1.2，7.5
*   Mac OS 7.6
*   Mac OS 8.0、8.1、8.5、8.6
*   Mac OS 9.0、9.1、9.2
*   苹果 OS X 10.0–10.11
*   macOS 10.12、10.13

在 7 台 Mac 电脑上

*   Performa 630(约 1994 年，摩托罗拉 68040)
*   动力 Mac G3 米色(约。1997，摩托罗拉 PowerPC 730)
*   动力 Mac G3 蓝色(约。1999 年摩托罗拉 PowerPC 730)
*   电源 Mac G4 数字音频(ca。2001，摩托罗拉 PowerPC 7400)
*   Mac mini G4(约。2005，摩托罗拉 PowerPC 7447)
*   苹果迷你 2009(英特尔酷睿 2 双核处理器 Penryn)
*   MacBook Air 2012(英特尔酷睿 i5/i7)

自 1984 年推出以来，Macintosh 系列计算机跨越了四个处理器家族中的三个。你可以在主图中看到成功，Mac OS 8 搜索工具夏洛克显示在 MacBook Air 运行 High Sierra 的 dock 中。

这个过程并不是没有故障，其中大部分与操作系统磁盘分区和格式有关。[Pierre]选择了一款 M.2 SATA 固态硬盘，通过适当的适配器，它可以作为并行 ATA 驱动器、串行 ATA 驱动器，或者在更现代的计算机中直接用作 M.2 SSD。让这个项目变得更具挑战性的是，[Pierre]想要录制过程的视频，这涉及到在所有各种升级过程中捕捉计算机屏幕。他在流程的每个阶段都保留了磁盘映像备份，因此他可以从错误中恢复，而不必从头开始。

最终停止旅程的是文件系统。[Pierre]的 SSD 开始使用 HFS 文件系统，但在 Power Mac G3 米色迁移阶段的某个地方，他不得不升级到 HFS+(扩展 HFS)文件系统，这不是一个胆小的人可以做的事情。在这个过程中，这个 HFS+文件系统也必须进行几次扩展和调整。但是旅程在 macOS 10.13 High Sierra 戛然而止。下一个版本 10.14 Mojave 需要 APFS 文件系统(不要与现在已经废弃的 AFP 文件系统混淆)。[Pierre]认为即使这样也是可以克服的，因为问题似乎源于 APFS 规定的 4096 字节的最小块大小。这似乎有可能通过克隆硬盘来克服，但这将违背他最初挑战的精神。

预先警告，休息下面的视频是整个过程的 2 小时“缩略”版本(DOS 到 Windows 10 的视频在 11 小时打卡)。我们不确定这有什么实际用途，但阅读这个过程和(皮埃尔)在这个过程中必须解决的问题确实很有趣。您在计算机上迁移系统驱动器的最长时间是多久？请在下面的评论中告诉我们。

 [https://www.youtube.com/embed/F4gpZx1ioNA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/F4gpZx1ioNA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

