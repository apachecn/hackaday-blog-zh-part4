# 在树莓馅饼上闲聊

> 原文：<https://hackaday.com/2020/07/12/making-smalltalk-on-a-raspberry-pi/>

今天，你可能不太想面向对象编程，它只是风景的一部分。但在几十年前，这是一项陌生而晦涩的技术。虽然有几种语言导致了我们今天使用的面向对象工具，但其中最有影响力的是施乐 PARC 的 Smalltalk 语言。[Michael Engel]采用 Smalltalk VM 的 C++实现、完整 Smalltalk 系统的一些字节码、一个 Raspberry Pi“裸机”库，并制作了一个运行在裸 Raspberry Pi 上的 [Smalltalk 工作站](https://www.linkedin.com/pulse/relive-part-xerox-parcs-history-smalltalk-80-raspberry-michael-engel/)——甚至是一个 Pi 0。代码在 [GitHub](https://github.com/michaelengel/crosstalk) 上，并且被公认为是一项正在进行的工作。

闲聊很有趣——有时也很烦人——因为一切都是对象。几乎所有的东西。系统接管了整台机器。它提供了 GUI、编译器和运行时库。这可能就是为什么[Michael]很容易为他的项目放弃通常的 Linux 操作系统。

如果不想用备用闪存卡引导进入系统，有 [Smalltalk 80](https://www.gnu.org/software/smalltalk/) 版本运行在普通操作系统上。如果你以前没有做过 Smalltalk，该程序用户手册中的教程可能会对你有所帮助。

在 Smalltalk 中，即使是最低的整数也是完整的对象。在 Smalltalk 中，当您说“3+2”时，您实际上是在说，您有一个值为 3 的 integer 对象，它接收一个带有整数参数 2 的+消息。如果你试图用面向对象的原则来包装你的头脑，这是非常令人困惑的，尽管经过几十年的后见之明，它更有意义。Smalltalk 也做了很多推广图形用户界面软件的模型/视图/控制器设计。

我们以前看过面向对象的[状态机](https://hackaday.com/2015/11/14/object-oriented-state-machine-operating-system-goes-open-source/)，这是一个很好的用例。如果你想知道 PARC 对未来的预测有多准确，那就去看看所有演示之母[。](https://hackaday.com/2019/01/03/retrotechtacular-the-mother-of-all-demos-50-years-on/)