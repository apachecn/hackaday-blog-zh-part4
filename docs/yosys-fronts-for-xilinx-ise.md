# Xilinx ISE 的 Yosys 前端

> 原文：<https://hackaday.com/2019/12/13/yosys-fronts-for-xilinx-ise/>

我们总是惊讶于开源工具是如何超越他们的商业对手的。Verilog 合成的开源工具 Yosys 就是一个很好的例子。尽管 Xilinx ISE 设计套件接近于废弃软件，但许多人仍在使用它，因为它支持较旧的 FPGAs，而较新的工具不支持。它的 Verilog 解析器在追赶新标准方面有些慢，根据最近 GitHub 更新的[，Yosys 现在可以为 ISE 提供针对 Spartan 6、Virtex 7 和 Series 7 FPGAs 的文件。此外，对 Spartan 3、Virtex 2、4 和 5 也有一些支持，尽管那些还没有准备好。](https://github.com/YosysHQ/yosys/issues/448)

根据这篇文章，您将希望使用 synth_xilinx 命令以及与您的目标匹配的-ise 选项和 a -family 选项(即 Spartan 6 的 xc6s)。在输出端，您将使用 write_edif 命令编写一个 EDIF 文件。

这并不是说为 ISE 处理 Verilog 的 Xilinx XST 解析器很糟糕。然而，它确实在一些功能上落后了，如果它不工作…太糟糕了。Xilinx 对 ISE 及其变体的关注度较低，而支持 Vivado，后者不支持许多旧芯片。有了 Yosys，这个项目就有了一个活跃的社区，如果有必要，你可以自己动手解决任何问题。您至少可以使用源代码来回答假设问题。

我们已经介绍了一些用于 [Yosys 和晶格目标](https://hackaday.com/2018/10/03/icestorm-tools-roundup/)的工具和技巧。如果你想开始，总有我们的[训练营](https://hackaday.com/2018/08/06/learn-fpga-fast-with-hackadays-fpga-boot-camp/)。