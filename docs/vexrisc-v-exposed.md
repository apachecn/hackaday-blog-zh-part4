# VexRISC-V 暴露

> 原文：<https://hackaday.com/2018/12/08/vexrisc-v-exposed/>

如果你想使用 FPGAs，你几乎总是会使用像 Verilog 或 VHDL 这样的 HDL。这些是抽象层，就像使用 C 编译器对机器语言或汇编代码一样。还有其他的王位挑战者，比如 SpinalHDL，他们拥有数量不多但热情的追随者。[Tom]发表了一篇关于 [VexRISC-V CPU 如何利用 SpinalHDL](https://tomverbeure.github.io/rtl/2018/12/06/The-VexRiscV-CPU-A-New-Way-To-Design.html) 来构建一个极其灵活的系统，其效率与普通 Verilog 一样高。他说这个例子真正展示了为什么你应该使用 SpinaHDL。

就像传统的编程语言一样，很容易找到吸引一点注意力的利基语言，这些语言要么开始流行(比如 C++、Java 或 Rust ),要么逐渐消失。问题是你永远也不会知道哪些会成为主流，哪些只是昙花一现。SpinalHDL 是下一个大事件吗？我们不知道。

[汤姆]也很有资格写这个。他有一个 RISC-V 设计，MR1，相比之下，SpinalHDL 实现更好。他想知道为什么。这篇文章是他探索的结果。

SpinalHDL 使用 Scala——一种面向对象的编程语言，实际上是一组生成 HDL 的库。这意味着你可以用 Verilog 或 VHDL 来处理你的普通工具，或者你甚至可以把它和传统的模块混合在一起。该语言的支持者声称，使用它可以生成高效的 HDL，不会导致你的设计变得更慢或更大。

值得转行吗？我们不知道。值得一看吗？大概吧。我们最近实际上[研究了 VexRISC-V](https://hackaday.com/2017/07/21/vexriscv-a-modular-risc-v-implementation-for-fpga/) ，但没有这么详细。如果你不喜欢 Scala，但喜欢这种方法， [MyHDL](https://hackaday.com/2012/06/13/myhdl-python-programming-option-for-fpga/) 有点像 SpinalHDL，但基于 Python。