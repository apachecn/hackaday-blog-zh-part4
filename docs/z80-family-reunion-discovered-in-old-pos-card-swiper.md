# 旧 PoS 刷卡器发现 Z80 家庭团聚

> 原文：<https://hackaday.com/2021/06/14/z80-family-reunion-discovered-in-old-pos-card-swiper/>

[Ben Heck]在 Goodwill 商店找到一个旧的刷卡销售点盒子，把它带回家，[把它拆下来看看里面有什么](https://www.youtube.com/watch?v=TDYfl-vJvY4)。他找到了一台完全可用的基于 Z80 的单板计算机。事实上，Z80 芯片有四个家族:CPU 本身、DART 芯片(双 UART)、PIO 芯片(并行输入/输出接口)和 CTC 芯片(计数器/定时器电路)。这还不是全部——还有一个固定电话调制解调器、一个实时时钟、32K 内存和 UV-EPROM。这个组件的第二个 PCB 有一个巨大的 16 键键盘和一个 16 字符真空荧光字母数字显示器。所有这些都是为了 2.99 美元的低价。

![](img/fa1206660c48caecc212911a210e5c34.png)

当然[本]将在未来挖掘 Z80 系统，但在这个视频中，他试图使显示工作。OKI 半导体控制器驱动 VFD。在找到数据表后，[Ben]将其连接到 Arduino 并编写了一个快速程序。仅仅几分钟后，他就征服了显示屏，在屏幕上任何他想要的地方以任何他想要的亮度画出样本文本。

你永远不知道你会在像这样的旧设备里发现什么。你可能会找到一个没有文档的专有 ASIC，或者像[Ben]在这里所做的那样，你可以找到一个全功能的嵌入式计算机。如果[Ben]能够开发一个基于 RAM 的仿真器来取代 32K UV-EPROM，他将拥有一个用于 Z80 项目的完美评估板。

如果你发现了这样的宝藏，请在评论中告诉我们。还有，如果你找到了这块板，你会怎么用？感谢读者[nika bar lovi]提供的提示。

 [https://www.youtube.com/embed/TDYfl-vJvY4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/TDYfl-vJvY4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

