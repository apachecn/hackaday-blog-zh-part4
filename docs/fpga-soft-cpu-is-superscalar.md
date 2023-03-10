# FPGA 软 CPU 是超标量的

> 原文：<https://hackaday.com/2019/06/22/fpga-soft-cpu-is-superscalar/>

我们承认:当我们在 FPGA 上看到自制的 CPU 设计时，这是一个简单的设计，在 20 世纪 70 年代或 80 年代不会引起任何惊讶。然而,(亨利·王的)设计并非如此。他的 x86 式设计做超标量乱序执行，就像大型商用现代 CPU 一样。当然[亨利]为英特尔设计 CPU 架构，所以这并不奇怪。你可以在下面的视频中看到[关于设计的详细介绍](https://www.youtube.com/watch?v=vhHR6fNHyG8)。你也可以阅读整个[论文项目](https://tspace.library.utoronto.ca/handle/1807/80713)。

[Henry]首先介绍了 FPGAs 和软处理器。他还介绍了使用多指令发布来提高 CPU 的虚拟时钟速率。换句话说，如果一个 100 MHz 的 CPU 一次可以执行一条指令，理论上它不会比一个 50 MHz 的 CPU 一次可以执行两条指令快。当然，试图同时做两件事会有一些开销，所以这不会完全正确。

我们的第一印象是 x86 指令集实现起来相对困难。但是[Henry]指出，如果你能提供一个健壮的实现——它可以包括一些更难的部分的仿真，比如浮点运算——你就可以运行大量的软件，而不需要任何修改。

我们对在设计进入 FPGA 之前使用 Bochs(一个 CPU 模拟器和一个已知良好的 x86 模型)验证设计的方法印象深刻。当您必须实现像寄存器重命名和分布式矩阵调度器这样的技术时，这尤其有用。

如果你以前从未从事过 CPU 设计，这可能不是一个好的选择。但是如果你准备从玩具 CPU 转移到更大的东西，这里有很多好的信息。需要更多的 FPGA 指导吗？试试我们的[训练营](https://hackaday.com/2018/08/06/learn-fpga-fast-with-hackadays-fpga-boot-camp/)。如果你更愿意黑掉 [RISC-V](https://hackaday.com/2018/11/26/risc-v-cpu-gets-a-peripheral/) ，我们也已经考虑过了。

 [https://www.youtube.com/embed/vhHR6fNHyG8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/vhHR6fNHyG8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

