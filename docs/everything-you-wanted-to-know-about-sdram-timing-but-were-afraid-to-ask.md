# 你想知道但不敢问的关于 SDRAM 时序的一切

> 原文：<https://hackaday.com/2022/08/05/everything-you-wanted-to-know-about-sdram-timing-but-were-afraid-to-ask/>

从事我们的爱好或职业的一个问题是，人们认为如果你能用芯片制造一台电脑，你一定知道他们最新的笔记本电脑的所有细节。与 DDR4 内存相比，我们处理的大多数内存都非常简单，如果您曾经尝试过调整内存，您会知道一个好的 BIOS 有几十种内存设置。[实际上是硬核超频]对典型的 DDR 4 数据表有一个很好的描述，你可以在下面的视频中观看。

当然，他指出，知道所有这些真的对内存超频没有太大帮助，因为没有试错，你无法真正预测复杂的影响。然而，我们大多数人喜欢理解我们随机扭曲的旋钮。最重要的是，视频的一个主题是 DRAM 是愚蠢和简单的。如果你曾经想过在一个项目中使用它，这可能是一个好的开始。

毕竟，只有 18 条命令——比典型的微控制器少得多。如果自我设计吸引了你，你会对他没有涵盖自刷新和省电模式感到有点失望，但视频将为你开始学习更多内容提供一个良好的基础。

即使在这 18 个命令中，仅仅为了读和写，您只需要少量的命令。然而，如果你想自己卷，你会需要相当多的。如果你的目标是 FPGA，有许多基于 FPGA 的控制器，如[这个](https://www.joshbassett.info/sdram-controller/)，可以帮助你了解更多。

不要忘记 [DDR5](https://hackaday.com/2020/01/29/ddr-5-ddr-4-we-hardly-knew-ye/) 会让你很快购买新的 RAM，然后你就会有很多空闲的 DDR4。当然，现在你可能更喜欢围绕 [NVMe](https://hackaday.com/2021/01/13/nvme-blurs-the-lines-between-memory-and-storage/) 进行设计，这是一种内存和一种磁盘驱动器。

 [https://www.youtube.com/embed/105IJiGbGsg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/105IJiGbGsg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

