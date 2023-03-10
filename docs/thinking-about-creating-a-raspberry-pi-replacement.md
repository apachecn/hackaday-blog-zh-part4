# 想创造一个树莓派的替代品？

> 原文：<https://hackaday.com/2020/10/20/thinking-about-creating-a-raspberry-pi-replacement/>

如果你曾经想尝试为自己创建一个类似树莓派的主板，你应该看看[Jay Carlson 的]对 10 个不同的支持 Linux 的 SOC 的评论。回到 20 世纪 60 年代，一台计算机是多个冰箱大小的盒子，有成千上万的互连，从头开始建造一台计算机对大多数人来说只是一个梦想。后来集成电路出现了，把所有最重要的部件都装在一个相对便宜的集成电路封装中，自制计算变得容易多了。片上系统(SoC)更进一步，使得创建整个系统比以往任何时候都更容易，就像 Pi 及其许多竞争对手一样。

就在几年前，制作 SoC 还是一个大项目，因为供应商通常不愿意向公众发布文档。另外，大部分器件采用球栅阵列(BGA)封装。BGA 器件很难加工，需要多层印刷电路板。当然，你不能把它们插到典型的无焊试验板上。但是使用这些相对较大的 BGA 并不困难，多层板现在相对便宜。[Jay]报告说，他得到了便宜的 PCB，并使用热板来构建每个电路板，并就如何做到这一点提出了一些明智的建议。

尽管他看到了 10 种不同的芯片，但他最终制作了大约 25 块电路板，并故意避免使用 PCB 布局示例。这让他可以优化手工组装，并尝试一些不同的策略，如内存布局。[Jay]指出这些板更多的是用于评估而不是使用。他没有在主板上安装任何在正常工作的系统中可能需要的外围设备。他只包括了将芯片引导到 Linux 所必需的东西。

[Jay]在文章中用了很长的篇幅谈论为什么你可能想使用 Linux，为什么你可能不想使用 Linux，以及为什么 Raspberry Pi 4 可能不是你的最佳选择，这取决于你的设计目标。他还给出一个关于简化单芯片 DDR 存储器布局的教程。

这是出了名的难做，邮报承认对于多芯片设计来说，这更难。然而，在涉及的速度和建议的拓扑结构下，[Jay]能够构建几个工作设计，甚至能够超频内存。结论是，对于主板上 DRAM 信号时序的所有恐慌，其中一些可能是不必要的严格，购买已有 RAM 的模块可能是不必要的昂贵。当然，部分原因是因为这些处理器都没有以非常高的速度运行，也没有过于复杂和快速的 RAM。

帖子的前半部分充满了这样的信息，但没有对实际部件进行任何测试。当你看到下半部分时，你会看到他使用了来自 Microchip、ST、NXP、Ti、Allwinner 等厂商的 10 种不同的芯片。我们对完成的工作量印象深刻，包括基准测试。实际写起来令人印象深刻，每个部分都有自己的怪癖，如 Allwinner 部分只能处理第一个 16MB 的闪存。他甚至还放了一段视频，你可以在下面看到。

老实说，我们大多数人不会这样做。我们将继续购买主板。然而，我们看到有人从 Pi 上偷了 SoC，然后[把它放到自己的板上](https://hackaday.com/2019/07/11/make-a-compatible-raspberry-pi-clone-but-your-pi-must-die/)。如果你不喜欢 ARM SoC，也有 [x86 主板](https://hackaday.com/2019/06/06/the-atomic-pi-is-it-worth-it/)。

 [https://www.youtube.com/embed/Ybbu-YnBrCQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Ybbu-YnBrCQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

