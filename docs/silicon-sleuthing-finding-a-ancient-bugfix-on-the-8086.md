# 硅侦查:在 8086 上找到一个古老的 bug

> 原文：<https://hackaday.com/2022/11/28/silicon-sleuthing-finding-a-ancient-bugfix-on-the-8086/>

很少有 CPU 像 8086 那样具有持久的影响力。很难相信，当你的现代台式电脑启动时，它可能会认为它是 1978 年的 8086，直到一些软件将其转换到更现代的状态。然而，当[Ken]检查 8086 芯片时，他注意到芯片的[部分与其余部分](https://www.righto.com/2022/11/a-bug-fix-in-8086-microprocessor.html)不一样。原来，英特尔在 8086 的原始版本中有一个错误。在那些日子里，你不能修补微码。它更像一个 PC 板——你必须改变布局，并制作一个新的来修复它。

受影响的区域是分组解码 ROM。该区域负责根据指令所需的解码类型对指令进行分类。虽然它被标记为 ROM，但它更像是一个可编程逻辑阵列。这个 bug 相当强烈。如果在 MOV SS 或 POP SS 指令之后出现中断，就会发生大混乱。

这个 bug 是设计师犯的一个简单的错误。假设你想完全改变堆栈指针寄存器。你必须加载堆栈段寄存器(SS)和堆栈指针(SP)。问题是，加载这两者并不是原子操作。也就是说，它需要两条不同的指令，每个寄存器一条。如果中断发生在加载 SS 之后但在加载 SP 之前，那么中断上下文将在某个不正确的存储位置结束。

您可以用几种方法来解决这个问题。英特尔的做法是让两条可以修改 SS 的指令将中断推迟一个指令周期。这将允许您在中断发生之前加载 SP。本质上，它使 MOV SS 或 POP SS 指令保护下一条指令，以便您可以编写原子操作。事实是,“修复”会停止任何段寄存器加载的中断。[Ken]注意到这是不必要的，在较新的处理器上的后来的实现只是停止 SS 的中断。

你可能认为你可以把这个推给程序员。例如，您可以坚持在中断被禁用的情况下改变堆栈指针。问题是 8086 有一个不可屏蔽的使用堆栈的中断，软件不能阻止它。

上世纪七八十年代的失败分析很有趣。光学显微镜可以完成大部分工作。如果你有一个带 T2 EDS T3 附件的扫描电镜 T1，你几乎可以做任何事情。一个[螺旋钻](https://en.wikipedia.org/wiki/Auger_electron_spectroscopy)和一个[模拟人生](https://en.wikipedia.org/wiki/Secondary_ion_mass_spectrometry)会让你处于世界级的实验室状态。如今，器件的几何尺寸小了几个数量级，封装中的芯片上下颠倒，而且有几十层——我们不知道如何在现代芯片上实现所有这些。

我们喜欢[肯]的 CPU[拆卸](https://hackaday.com/2022/09/23/exploring-texas-instruments-forgotten-cpu/)。他也在[从事更大的事情](https://hackaday.com/2019/09/23/secrets-from-a-1969-analog-computer/)。