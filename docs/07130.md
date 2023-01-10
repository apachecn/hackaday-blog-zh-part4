# 软核 CPU 比较

> 原文：<https://hackaday.com/2020/07/12/softcore-cpu-comparison/>

蒙蒂·派森曾经画了一个草图，人们试图在十五秒内总结普鲁斯特。虽然总结八个基于 FPGA 的 CPU 几乎是令人生畏的，但[jaeblog]做得很好，[给出了 CPU 如何与 Xilinx Vivado 工具链和 Digilent Arty 板一起工作的快速草图](https://justanotherelectronicsblog.com/?p=705)。

这八个 CPU 是:VexRiscv、LEON3、PicoRV32、Neo430、ZPU、Microwatt、S1 Core 和 Swerv EH1。

比较标准非常实用:每个 CPU 都有一个 C 编译器(gcc 或 llvm ),没有 CPU 绑定到特定的 FPGA。其中两个 CPU 不适合 Arty board，因此它们的比较更具理论性。还有其他的考虑，比如速度、文档、调试支持等等。

有趣的是，看到了各种各样的 CPU，从一些非常成熟的处理器到一些新的产品，虽然这些评价有些主观，但它们似乎是公平的，代表了您自己要寻找的东西。如果你想亲自尝试，你也可以获得[测试代码](https://github.com/riktw/SoftcoreComparisons)。

获胜者？这篇文章确定了三个可能是首选的 CPU，尽管没有一个是完美的。当然，你的经历可能会有所不同。

如果你想要一个简单的介绍来添加东西到软 CPU，这个 [RISC-V 项目](https://hackaday.com/2018/11/26/risc-v-cpu-gets-a-peripheral/)是可行的。或者，如果你更喜欢 SPARC，看看[这个项目](https://hackaday.com/2019/11/01/sparc-cpu-in-a-cheap-fpga/)。