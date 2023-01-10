# 你可以制作一张 Linux 名片

> 原文：<https://hackaday.com/2022/07/14/a-linux-business-card-you-can-build/>

这是一个时代的标志，德米特里为他的名片上的新 Linux 设计的标准之一是使用你在当前组件短缺期间实际上可以找到的部件。最终的主板使用 ATSAMD21 芯片，并模拟 MIPS 机器来引导 Linux。

除了构建细节之外，我们还喜欢[Dmitry]概述了他的决策的许多原因。关于整个系统实际上是如何工作的，也有相当多的细节。例如，通过使用 0.8 mm PCB，该板可以接受 USB-C 电缆，无需额外的连接器。MIPS MMU 也有很好的解释，不要忘记 MIPS 是 RISC-V 的起源，所以许多 MIPS 核心细节也适用于 RISC-V(但[不是 MMU](https://www.sifive.com/blog/all-aboard-part-9-paging-and-mmu-in-risc-v-linux-kernel) )。你还会发现一些[对 ATSAMD21 的 DMA 系统](https://www.sifive.com/blog/all-aboard-part-9-paging-and-mmu-in-risc-v-linux-kernel)的批评。这似乎是为了节省芯片面积，DMA 系统将配置数据存储在用户存储器中，每次切换频道时都要加载和卸载这些数据。

在这篇文章的结尾，你会觉得这可能是[Dimitry]最后一个 ATSAMD21 项目。但我们不得不承认，结果似乎很好。这不是我们看到的第一个[名片 Linux 版本](https://hackaday.com/2019/12/24/now-even-your-business-card-can-run-linux/)。这肯定让我们想起了曾经见过的 [MIDI 控制器卡](https://hackaday.com/2018/05/11/stylish-business-card-with-a-stylophone-built-in/)。