# FPGA 6800 使用 Python 工具箱

> 原文：<https://hackaday.com/2019/12/27/fpga-6800-uses-python-toolbox/>

通常，当你想到在 FPGA 上设计或重建 CPU 时，你会认为你必须使用 Verilog 或 VHDL。还有其他选择，但这是 FPGA 配置中最大的两个因素。[Robert Baruch]有一个多部分系列[，其中他使用 nMigen](https://www.youtube.com/watch?v=85ZCTuekjGA)——一个 Python 工具箱——来重新创建一个 6800 CPU，就像许多老式视频游戏和弹球机中使用的 CPU 一样。

与一些试图将某种语言编写的软件转换为 FPGA 配置的工具不同，nMigen 使用 Python 作为脚本语言来创建 FHDL 代码。这在概念上类似于 VHDL 或 Verilog，但放弃了事件驱动的范式，而是选择允许设计人员显式调用同步和组合逻辑。

有趣的是，该工具基于 Yosys，因此它可以针对几个 Lattice 器件以及来自 Intel/Altera 和 Xilinx 的 FPGAs。原来 nMigen 中的 n 代表新的，您可能会发现一些针对常规旧 Migen 的[文档很有用。](https://m-labs.hk/gateware/migen/)

至于 6800，它是业余爱好计算机中使用的较老的 CPU 之一。8 位 CPU 有大约 72 条指令，这取决于你如何计算它们。这是在精简指令集盛行之前，所以实现一个丰富的指令集需要一点额外的工作。

还有其他的 Python 选项，例如 [MyHDL](https://hackaday.com/2012/06/13/myhdl-python-programming-option-for-fpga/) 和 [PyCPU](https://hackaday.com/2012/06/11/programming-fpgas-with-python/) 。你甚至可以尝试使用[。网](https://hackaday.com/2019/12/15/net-to-fpga-with-hastlayer/)。

 [https://www.youtube.com/embed/85ZCTuekjGA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/85ZCTuekjGA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

