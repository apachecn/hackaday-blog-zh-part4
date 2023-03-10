# 通量引擎读取软盘

> 原文：<https://hackaday.com/2019/02/19/flux-engine-reads-floppies/>

有点矛盾的是，我们以数字方式存储越来越多的信息，但每年越来越多的信息变得越来越难以获取。曾经常见的各种磁带和磁盘上的数据现在被困在介质上，因为缺少读取数据的硬件。你有压缩驱动器吗？你有能让它工作的电脑吗？软盘也是个问题。你可能认为只要有一个 USB 软驱就能打败系统。虽然这些确实存在，但它们通常不会读取奇怪的格式。也就是除了 Flux Engine，一个[开源的 USB 软驱](http://cowlark.com/fluxengine/)。

该设备使用 15 美元的 Cypress 开发板和一些布线(当然，还有 3.5 或 5.25 软盘驱动器)。目前，[固件](https://github.com/davidgiven/fluxengine)只支持对 IBM 标准磁盘和 Acorn DFS/ADFS 磁盘的只读访问。还能读写兄弟文字处理器磁盘。然而，作为开源软件，它可以做得更多。作者[David Given]正在寻找 Commodore 1541 和苹果 CLV 磁盘，以便他可以让这些工作。他还提出，如果你愿意借给他一张磁盘，他可以尝试其他格式。

该软件使用 libusb，已知可以在 Linux 和 Windows 上与 Cygwin 一起工作。它也应该适用于 OSX。然而，您将需要某种 Windows 机器来构建 Cypress 固件，因为 Cypress 工具在其他地方不能工作。[David]因此想要更换处理器，但如果他这样做了，我们猜测他会错过 PSoC 功能块。

这个设计实际上相当简单。固件仅测量通量转换之间的时间，并将它们发送到连接的 PC。所有繁重的工作都发生在 PC 上，这意味着分析和解码新格式应该很容易。虽然写作是可能的，但似乎还需要做更多的工作来使其可靠。[大卫]评论说，你真的需要一个真正的驱动器来测试你的写作，这样你就不会写只有你可以回读的东西。有道理。

这肯定比我们看到的[最后一个方法](https://hackaday.com/2019/01/08/preserving-floppy-disks-via-logic-analyser/)更加用户友好。我们不得不怀疑[大卫]是否考虑过[8 英寸软盘](https://hackaday.com/2017/01/22/an-eight-inch-floppy-for-your-retrocomputer/)。