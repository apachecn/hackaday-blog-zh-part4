# 致力于 FPGA 开发

> 原文：<https://hackaday.com/2019/10/28/chisel-away-at-fpga-development/>

大多数时候，如果你想为 FPGA 开发，你可能会转向 Verilog 或 VHDL。这两者都很有能力，但它们也牢牢地植根于以今天的标准来看已经过时的语言中。已经有相当多的尝试将这些语言作为其他工具的输出——无论是高级语言还是图形工具。最近的一项努力是以凿子开始的工具链。

Chisel 背后的想法是为 Scala 提供类似 Verilog 的结构。如果你愿意，你可以把它作为一个“超级 Verilog ”,利用类和其他特性。然而，Chisel 也允许你创建生成器，根据你调用它们的方式产生不同的输出 Verilog。的确，你可以用 Verilog 模块来做这些，但是用 Chisel 要容易得多。Chisel 使用 Firrtl 将您要求它做的事情转换成 Verilog，用于不同的 FPGA 和 ASIC 目标。

如果你读了主页上的一些链接，你会发现他们承认你可以做任何你在 Chisel 中可以做的事情。事实上，到目前为止，Chisel 还缺少一些功能，尽管你可以使用 Verilog 黑盒来解决这些问题。但是，这就好比说为什么要用 C++而不是 C，或者用 C 而不是汇编语言。早期的 C++编译器发出 C，所以你完全可以用 C 做 C++做的任何事情——只是不总是很容易。汇编语言也是如此。显然，你可以在汇编中做任何事情。但是更高层次的抽象可以让你更有效率。

即使不懂 Scala 也可以学习 Chisel，根本不用安装[任何软件](https://mybinder.org/v2/gh/freechipsproject/chisel-bootcamp/master)。甚至有一些基于模拟的验证工具可用。当然，值得记住的是，还有许多类似的竞争对手，包括 [SpinalHDL](https://hackaday.com/2018/12/08/vexrisc-v-exposed/) 和 [MyHDL](https://hackaday.com/2012/06/13/myhdl-python-programming-option-for-fpga/) 。时间会证明这些方法是否会被广泛采用。