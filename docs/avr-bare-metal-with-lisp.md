# 带 Lisp 的 AVR 裸机

> 原文：<https://hackaday.com/2021/05/04/avr-bare-metal-with-lisp/>

程序员分两种:不使用 Lisp 的，每半年需要新括号键帽的。Lisp 是你要么真的喜欢要么真的讨厌的语言之一。如果你喜欢它，你可能已经检查过 ulisp，它运行在 AVR 和 ARM 种类的 Arduino 板上，以及 ESP 芯片、RISC-V 等。最近的一次更新允许该语言将[汇编器插入 AVR 程序](http://www.ulisp.com/show?3IUO)。

我们可能不需要说服任何阅读 Hackaday 的人为什么添加汇编程序是一件好事。它似乎也能很好地与环境集成，所以您可以用 Lisp 编写汇编宏，这提供了许多可能性。

当然，格式和你的普通汇编器不一样。毕竟，Lisp 应该代表“大量恼人的虚假括号”此外，您的代码需要与位置无关，因为您永远不知道它在哪里加载。

这里有一个简单的例子:

`; Greatest Common Divisor
(defcode gcd (x y)
swap
($movw 'r30 'r22)
($movw 'r22 'r24)
again
($movw 'r24 'r30)
($sub 'r30 'r22)
($sbc 'r31 'r23)
($br 'cs swap)
($br 'ne again)
($ret))
(gcd 3287 3460)` 
[网站上还有更多例子](http://www.ulisp.com/show?3IUM)，包括直接 I/O 寄存器操作。

我们已经看到[徽章运行 ulsip](https://hackaday.com/2019/01/10/program-this-badge-in-lisp/) 。不过说实话，我们会对第四个[和第三个](https://hackaday.com/2017/08/04/take-the-blue-pill-and-go-forth/)同样满意，而且它对我们的括号键来说更容易。