# 信号发生器使用 FPGA

> 原文：<https://hackaday.com/2018/08/11/signal-generator-uses-fpga/>

虽然有一些例外，但 FPGAs 主要是数字设备。然而，许多 FPGA 应用处理模拟数据，因此您经常会看到 FPGA 被模拟和数字转换器包围。这种情况非常普遍，以致于 FPGA 工具的生产商 Opal Kelly 为这种互连设备推出了 SYZYGY 开放标准。Opal Kelly 的暑期实习生[Armeen]使用 Xilinx FPGA 和符合 SYZYGY 标准的数模转换器制作了一个非常有趣的基于开源 [FPGA 的信号发生器](https://www.opalkelly.com/high-performance-fpga-based-signal-generator-using-the-xem7320-frontpanel-and-syzygy-dac/)。

如你所料，[Armeen]在项目中使用了大量的 Opal Kelly 硬件和软件。但是 Verilog 代码(可在 [GitHub](https://github.com/SYZYGYfpga/xem7320-syzygy-samples/tree/master/SignalGenerator) 上获得)显示了许多有趣的东西，包括一些使用 Xilinx CORDIC IP 的非常实用的示例代码，这是使用数字逻辑进行高阶数学运算的一种很好的方式。

了解 AM 和 FM 的工作原理是对 FPGA 中信号合成的一个很好的介绍。如果不想用 Xilinx IP，可以在 [OpenCores](https://opencores.org/project/cordic) 上找几个 CORDIC 内核。总的来说，如果你想了解 FPGAs，这是一个很好的中间项目。它足够复杂，可以向你展示一些实用的东西，但又不会复杂到让你感到沮丧。当然，Xilinx IP 中包含了许多功能，您可以认为这类似于使用 C 或 Java 库。

顺便说一下，SYZYGY 是一个免费许可的规范。它应该是简单 PMODs 和高速 FMC 板之间的桥梁。甚至有一个开源平台板来支持它。然而，据我们所知，目前只有 Opal Kelly 为它提供插件，所以它到底受欢迎还是不受欢迎还有待观察。

随着 Arduino 加入竞争，FPGAs 最近受到了很多压力。如果你需要一些东西来开始，在 Hackaday.io 上查看[我们的新兵训练营系列](https://hackaday.com/2018/08/06/learn-fpga-fast-with-hackadays-fpga-boot-camp/)