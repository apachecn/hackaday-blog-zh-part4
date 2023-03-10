# 由 74HC 芯片制成的 CPU 是一个辉煌的烂摊子

> 原文：<https://hackaday.com/2019/05/09/cpu-made-from-74hc-chips-is-a-glorious-mess/>

你有没有开始过一个项目，你觉得它获得了自己的生命？保罗·康斯坦丁诺的这个项目是在试验板上的一个名为“追梦人”的完整 CPU，是一个美丽的数字丛林。最重要的是，它可以连接到模拟 VGA 显示器。多酷啊！

设计 ALU 和 CPU 是数字设计专业学生的典型练习，使用 VerilogHDL 或 VHDL 完成。它涉及到创建一个 ALU，可以加，减等，而控制单元管理数据移动等。还有一个存储器提取和指令解码，由解复用器和一组触发器组成，这些触发器构成寄存器和标志。它们就像听起来一样复杂，甚至更复杂。

[保罗·康斯坦丁诺]使用 74HC 逻辑芯片在 Eagle 中将整个事情设计成一个原理图。为了制造它，他使用了试验板而不是印刷电路板。从总线解码器到控制外部 VGA 显示器，一切都是使用跳线完成的。我们不久前确实报道过这个项目的视频，但是这次更新增加了一个显卡接口。

CPU 更新 VGA 卡上的显示缓冲区，在下面的视频中显示了缓慢而稳定的更新。电线丛林可以驱动显示器的事实令人惊叹。从那以后，他开始研究 16 位版本的处理器，我们希望看到有人能更上一层楼。

对于那些更习惯于 PCB 的人来说， [Z80 会员卡项目](https://hackaday.com/2017/09/15/the-1980s-called-asking-for-the-z80-membership-card/)对于 [8 位计算机](https://hackaday.com/2016/11/18/the-basic-issue-with-retro-computers/)爱好者来说是一个很好的构建。

感谢[模拟工程师]的提示。

 [https://www.youtube.com/embed/Uvvsaj7BBzo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=21&wmode=transparent](https://www.youtube.com/embed/Uvvsaj7BBzo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=21&wmode=transparent)

