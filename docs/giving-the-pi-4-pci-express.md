# 给予 Pi 4 PCI Express

> 原文：<https://hackaday.com/2019/07/10/giving-the-pi-4-pci-express/>

Raspberry Pi 4 的发布为我们带来了一个新的 SoC，高达 4g 的内存，最重要的是，摆脱了那种简简单单的 USB 到 USB 和以太网解决方案。Raspberry Pi 4 有一个埋在一些芯片下的 PCI Express 接口，如果你非常擅长焊接[，你可以将 PCIe x1 设备添加到新的最佳单板计算机](http://mloduchowski.com/en/blog/raspberry-pi-4-b-pci-express/)。

[Thomasz]看了看 Raspberry Pi 4，发现新的 USB 3.0 芯片连接到 SoC 上的 PCI Express 接口。也就是说，如果您移除这个芯片，并且您有一些非常细的线，您可以插入一个真正的 PCI Express 插槽。用热风枪去除芯片很容易，尽管有几个瓶盖被弄得一团糟。把它扔进超声波清洗器里，你就有一块空白画布来施展 PCI 魔法了。

这种方法需要六根线或三个差分对，有一个参考时钟、一个通道 0 发射和一个通道 0 接收。从 PCI Express riser 开始向后工作，[Thomasz]找到了这些连接，并焊接了一些电线。在 Pi 端，一些电容需要符合 PCI Express 规范，但焊接不算太差。你可以用熨斗上的小尖头和显微镜做很多事情。

Pi 已成功连接到 PCI Express riser 卡，以及接地、5V、链路重新激活和电源良好信号的线路。剩下要做的唯一事情就是插入 PCI 卡并进行测试。这并不像预期的那样顺利，因为 PCI Express 适配器不喜欢被 Raspberry Pi 内核枚举。在随后的实验中，Adaptec SAS 控制器工作正常。这是否意味着 Pi 的外部显卡？不，不完全是；这只是 PCIe 的一条车道，现代显卡需要 x16 插槽才能获得最佳性能。然而，如果你曾经想要一个 SCSI 卡作为 Pi，这是最好的选择。