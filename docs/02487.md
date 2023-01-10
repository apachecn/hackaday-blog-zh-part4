# Gigatron TTL 微型计算机如何工作

> 原文：<https://hackaday.com/2019/03/25/how-the-gigatron-ttl-microcomputer-works/>

大约一年前，当 Hackaday 和 Tindie 在纽卡斯尔举行的 Maker Faire UK 展会上，一位 York Hackspace 的成员向我们展示了一台有趣的逆向计算机。Gigatron 是一种功能齐全的家用电脑，你可能在 20 世纪 80 年代初就拥有这种电脑，但它的特殊之处在于它不包含微处理器。它没有 6502、Z80 或其他集成 CPU，只有简单的 TTL 芯片，甚至不包含 74181 ALU-in-a-chip。因此，你可能会认为它有一个足球场大小的 PCB，上面布满了无数芯片，但它只占用了 36 个 TTL 芯片、一个 RAM 和一个 ROM。它的 RISC 架构提供了解释，它的创始人(Marcel van Kervinck)最近很好地向我们展示了一段解释其操作的视频。

它是去年在荷兰的黑客酒店黑客营录制的，由 Gigatron 团队的另一半[Walter Belgers]负责交付。在这本书里，他提供了一个关于 RISC 计算机如何工作的引人入胜的纲要，不管你是否对 Gigatron 感兴趣，它仍然值得一看。我们听到了设计理念和哈佛架构的选择，解释了 CISC 和 RISC 之间的差异，然后我们开始一点一点地拆卸机器的工作原理。解释了指令的格式，然后是 10 片 ALU 的细节。

这款显示器与 20 世纪 80 年代典型的家用电脑不同，它有一个全彩色 VGA 输出，而不是更常见的 NTSC 或 PAL。作为一组 2 位电阻 DAC，硬件足够简单，但在运行显示器的同时留出足够的处理时间来运行程序的技巧却是那个时代的产物。例如，同步间隔用于驱动另一个音频 DAC。

其结果是那些可能发生的时刻之一，让我们一瞥 RISC 架构早于[Sophie Wilson]为橡子阿基米德设计的第一只手臂几年就到达消费者层面的世界。像这样的机器没有理由不能在 20 世纪 70 年代末制造出来，但正如我们所知，这个行业发生了完全不同的转变。它仍然是我们希望在 20 世纪 80 年代拥有的机器，但当然这并不妨碍我们现在拥有一台。你可以买一个你自己的 Gigatron，一旦你焊接了所有的通孔芯片，你就可以运行示例游戏，或者掌握一些我们见过的最简单的裸机 RISC 编程。我们不得不承认，我们动心了！

 [https://www.youtube.com/embed/QUfdASs82Lw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/QUfdASs82Lw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

