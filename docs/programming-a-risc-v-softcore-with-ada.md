# 用 Ada 语言编程 RISC-V 软核

> 原文：<https://hackaday.com/2018/10/08/programming-a-risc-v-softcore-with-ada/>

[morbo]联系我们，让我们了解 AdaCore 博客上的一个项目，该项目涉及用 Ada 对 PicoRV32 RISC-V 软核进行编程。软核本身运行在基于晶格 ICE40LP8K 的 [TinyFPGA-BX](https://www.crowdsupply.com/tinyfpga/tinyfpga-bx) FPGA 板上，我们[在过去](https://hackaday.com/2017/07/31/tinyfpga-is-a-tiny-fpga-board/)已经介绍过。

这篇博客文章描述了如何使用 GNAT Ada 编译器的社区版来设置开发环境，然后实现一个简单的示例项目来控制一条 WS28212b RGB LED 模块。有两个按钮可以改变灯光的动画和亮度。

源代码可以在[作者的 Github](https://github.com/Fabien-Chouteau/Ada-PicoRV32-example) 资源库中找到，包含了 Ada 源代码和用于 [PicoRV32 软核](https://github.com/cliffordwolf/picorv32)的 Verilog 源代码。为了构建这个项目，需要 [GNAT 编译器](https://www.adacore.com/download)，以及开源的 [iCE40 开发工具](http://www.clifford.at/icestorm/)来编译软核。

有一个视频演示了完成的示例项目，我们将它放在了休息时间的下方。

 [https://www.youtube.com/embed/3pFyhLzfvhY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/3pFyhLzfvhY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

