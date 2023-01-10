# 生活的游戏进行得非常快，如果你不使用定格，你可能会错过它

> 原文：<https://hackaday.com/2021/11/11/the-game-of-life-moves-pretty-fast-if-you-dont-use-stop-motion-you-might-miss-it/>

撇开 Munged Ferris Bueller 的话不谈，康威的《生命游戏》是我们都想得到的经典细胞自动机。通常的方法是遍历网格中的每个单元，将下一个状态计算到一个新的网格缓冲区中。[K155LA3]通过在 FPGA 的硬件中实现“生命的游戏”[开始扭转这种局面。](https://k155la3.blog/2020/10/09/conways-game-of-life-on-fpga/)

[K155LA3]的版本使用了来自 Berkley 和 RISCV 社区的新 HDL[凿子](https://www.chisel-lang.org/)。在幕后，Chisel 是带有一些定制库的 Scala，这些库知道如何将 Scala 概念映射到硬件上。总的来说，Verilog 和 VHDL 专注于表达硬件，然后在此基础上增加了抽象。Chisel 和其他较新的 HDL 语言专注于表达映射到硬件上的高级通用元素。FPGAs 已经将复杂的电路和硬件映射到 lut 和其他片上，那么另一个抽象层是什么呢？

本项目选用的 FPGA 是 Digilent Arty A7，带有 VGA Pmod，可将 RGB444 转换为模拟信号进行实际显示。[K155LA3]的实现让人印象深刻的只是它的速度有多快。即使以每秒 60 帧的速度运行，这也几乎是显示器所能处理的最快速度了。当然，你周围的大多数计算机可以以 60 fps 的速度模拟 60 x4 8 的网格。接下来，他没有将栅极逻辑连接到 60 Hz VGA 时钟，而是将其连接到 100 MHz 板外部振荡器。现在显示的每一帧中的每个像素包含超过一百万代。

不幸的是，即使是这个 60×48 的小网格也占据了 Artix-7 上 90%的 lut。在未来，我们希望看到更大的 FPGA 硬件实现能够[处理网格，这些网格可以容纳整个计算机](https://hackaday.com/2020/11/21/a-computer-in-the-game-of-life/)。自然，这不是 Hackaday 的第一个 [FPGA 版本的生命游戏。](https://hackaday.com/2012/04/12/conways-game-of-life-in-hd/)