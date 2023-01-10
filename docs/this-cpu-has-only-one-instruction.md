# 这个 CPU 只有一条指令

> 原文：<https://hackaday.com/2019/12/07/this-cpu-has-only-one-instruction/>

我们大多数人在某种程度上都熟悉基本 CPU 的操作，通常是通过接触我们项目中的微处理器类型。我们可以看看它的内部框图，了解它是如何工作的，看看寄存器和 ALU，遵循冯诺依曼架构的原则，并了解它有一个指令集，每个功能都有不同的指令。我们都知道这只是描述了一种类型的 CPU，因此看到其他的 CPU 总是很有趣的。[Ike Jr]然后有一个项目应该会提供很多兴趣，它是只有一条指令的 CPU。它只能将数据从一个地方移动到另一个地方，这似乎排除了任何计算的可能性。它究竟是如何工作的？

机器有一组寄存器和存储器，它通过在我们可能期望看到指令的地方有特定的寄存器来实现计算。例如，AND 寄存器是两个位置的堆栈，当它满时，计算它的两段数据的 AND，并将结果放入通用寄存器。这篇文章详细描述了 CPU 的运行，虽然世界不太可能整体转向这种架构，但这仍然是一篇非常有趣的文章。目前，这是一台存在于软件模拟中而不是硅中的机器，他正在努力发布它，以便不寻常的 CPU 的爱好者可以一试。

让寄存器进行计算的想法让我们想起了[传输触发架构](https://hackaday.com/2017/04/21/an-8-bit-transport-triggered-architecture-cpu-in-ttl/)机器，它不同于带有[更传统计算指令](https://hackaday.com/2012/09/05/mess-of-wires-is-actually-a-one-instruction-computer/)的单指令 CPU。

摘要 PCB 头文件图片:哈兰·夸林顿/MOD [ [OGL v1.0](https://commons.wikimedia.org/wiki/File:Computer_Circuit_Board_MOD_45153619.jpg) 。