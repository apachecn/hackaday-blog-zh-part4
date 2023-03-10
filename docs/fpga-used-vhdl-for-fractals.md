# FPGA 使用 VHDL 实现分形

> 原文：<https://hackaday.com/2018/12/09/fpga-used-vhdl-for-fractals/>

在 GitHub 上，[ttsiodras]想学 VHDL。所以他开始用一种算法来做 Mandelbrot 集合，然后[把它转移到 FPGA](https://github.com/ttsiodras/MandelbrotInVHDL) 中。因为速度，他能够完成实时缩放。你可以在下面看到结果的视频。

FPGA 板是一个 ZestSC1，板上有一个相对较旧的 Xilinx Spartan 3 芯片。不过，对于这样的任务来说，它已经足够强大了。

该项目不直接驱动显示器。它进行数学运算，将结果存储在板上 RAM 中，然后使用 ZestSC1 的 USB 端口向 PC 发送一个帧。目前，代码没有流水线，未来的任务是添加[流水线](https://hackaday.com/2018/06/12/real-world-pipelining-for-fpgas/),这样它就可以在每个时钟周期计算一个新像素，当然是在一些延迟之后。

repo 包含 VHDL 代码和一些 C++代码，可与评估板交互并显示结果。如果你有那块特殊的板，它将是一个不同项目的良好基础。

我们的 FPGA 新兵训练营使用 Verilog，但是如果你想学习 FPGA，他们仍然是一个很好的起点。这些概念仍然适用，最近添加的状态机模块将为您提供一个良好的开端，无论您使用何种语言。如果你渴望更多的 VHDL 数学，总有 [CORDIC](https://hackaday.com/2018/09/07/cordic-brings-math-to-fpga-designs/) 。

 [https://www.youtube.com/embed/yFIbjiOWYFY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/yFIbjiOWYFY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

