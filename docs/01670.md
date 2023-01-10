# 木制时钟到 FPGA 的转换

> 原文：<https://hackaday.com/2019/01/02/wooden-clock-to-fpga-conversion/>

[John]想要一个项目来帮助他学习更多关于 FPGAs 的知识。所以他开始用他的木制时钟——用 Arduino 制造——并用 Icestorm 将它移植到点阵 FPGA 上。有趣的是，他会带您了解他使用 Falsted 仿真器仿真设计的步骤，然后在 FPGA 中实现。因为他才刚刚开始，所以很有可能他会遇到和你一样的困难，有时这真的能帮你度过难关。你可以在下面看到一个视频，该项目的代码在 [GitHub](https://github.com/tuna-f1sh/wooden-bits-fpga) 上。

例如，在法尔斯塔德模拟了一个电路设计后，他意识到他可以制作一个大的计数器而不是几个模块，他将其与一个更模块化的方法进行了对比。他还遇到了一个对 Arduino 来说很简单但对 FPGA 来说很难的特性。他让它工作起来，但需要一些优化工作才能让一切都适合他正在使用的相对较小的 FPGA。

[John]最初的动机是想看看[Mattvenn]是如何为 RISC-V CPU 创建定制外设的。在这种情况下，您有一个完整的 CPU 供您使用，但是我们一致认为不把它作为第一个项目是明智的。

我们也喜欢先考虑逻辑，然后再考虑 Verilog 的方法。当然，如果你有很多经验，习惯上可以跳过这一步，只在 Verilog 中可视化你想要的逻辑，但这是随着经验而来的。

我们过去已经写了很多关于 Icestorm 项目的文章，包括我们自己的[入门教程](https://hackaday.com/2018/08/06/learn-fpga-fast-with-hackadays-fpga-boot-camp/)。但是有时选择例子和初始项目可以使事情变得更容易。

 [https://www.youtube.com/embed/U5OJ7-_I_tY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/U5OJ7-_I_tY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

