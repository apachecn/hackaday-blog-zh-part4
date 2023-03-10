# u 盘揭秘奇怪的 SD 卡心

> 原文：<https://hackaday.com/2020/07/17/usb-flash-drive-reveals-strange-sd-card-heart/>

许多黑客从背包底部挖出了一个旧的闪存盘，并拆开损坏的塑料盒来看里面。通常，你会看到 PCB 上的一些 SMD 芯片，以及一些无源器件、一个 LED 和一个 USB 端口。[[go ugh]发现了一些完全不同的东西，并为感兴趣的公众记录了下来。](https://goughlui.com/2015/04/05/teardown-optimization-comsol-8gb-usb-flash-stick-au6989sn-gt-sdtnrcama-008g/)

[![](img/298c55af6baea49715eb786a44edbc87.png)](https://hackaday.com/wp-content/uploads/2020/07/usdbsdsqr.jpg) 在 Comsol 8GB 盘里面，【高夫】发现了一整块 microSD 卡。人们可能会认为这是一个读卡器和伪装成普通闪存盘的 microSD，但事实远非如此。相反，该驱动器包含一个闪存控制器，通过通常在消费级卡上覆盖的测试点，将 microSD 卡作为原始 NAND 进行寻址。该驱动器似乎是由工厂生产的第二个 microSD 卡制造的，没有通过向公众销售的正常测试。

借助从虚假渠道获得的软件，[高夫]能够更深入地潜入闪存盘的内部。工程工具允许优化卡的容量或速度，以及不同级别的纠错。甚至可以让闪存驱动器模拟 U3 光盘驱动器，用于操作系统安装和其他目的。

这是一个很好的潜入如何 USB 驱动器工作在一个低水平，以及如何固件和硬件协同工作。我们以前也见过其他闪存驱动器黑客——[像这个简单的恢复技巧](https://hackaday.com/2013/11/27/repairing-dead-usb-flash-drives/)！