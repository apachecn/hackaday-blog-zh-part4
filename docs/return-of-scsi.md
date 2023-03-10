# SCSI 的回归

> 原文：<https://hackaday.com/2022/03/02/return-of-scsi/>

曾经有一段时间，高性能磁盘驱动器使用 SCSI——小型计算机系统接口——其他一切都是小儿科。现在，高级形式的 SCSI 仍然存在，但也有其他高性能的磁盘接口。但是一些老设备真的很喜欢它们经典的 SCSI 端口，于是[Adrian]决定尝试将其中一些连接到一些现代计算机上。你可以在下面的视频中看到他的表现。

这一尝试的关键是一个 USB 转 SCSI 适配器，这是不寻常的，但不是闻所未闻的，1999 年[阿德里安]遇到了一个。当然，你不得不怀疑一台现代计算机是否能支持这种设备，或者是否能从旧光盘上加载驱动程序。

这些适配器的一个问题是，SCSI 在当时是一种高性能总线，而相应的 USB 速度却没有那么多。并行 SCSI 使用差分信号，最高可达 320 MB/s。普通 USB 的重量为 1.5 MB/s。USB 2 做得稍好，但它需要 USB 3 才能超越旧的 SCSI 数据速率。当然，SCSI 变得像 USB 一样串行，现代串行连接 SCSI 甚至可以摧毁最快的 USB 设备。

我们怀疑你是否真的需要在日常生活中使用 SCSI 设备，但是你可能想要或者需要阅读一个显示出来的设备。另外，这也是对过去的一个有趣的观察。如你所料，寻找司机是一件非常痛苦的事情。事实证明，他可能不需要这么麻烦，因为 Windows 知道如何将其视为存储设备，但他没有马上发现这一点。

Android 似乎不太好用，尽管这可能是因为手机无法识别磁盘格式。

 [https://www.youtube.com/embed/APn4IhaYAlc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/APn4IhaYAlc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

