# Supercon 主题演讲:Megan Wachs 分解 RISC-V

> 原文：<https://hackaday.com/2020/01/27/supercon-keynote-megan-wachs-breaks-down-risc-v/>

2019 年 Hackaday 超级大会以 Megan Wachs 博士关于 RISC-V 主题的精彩绝伦、令人惊叹的[主题演讲拉开帷幕。她是 SiFive 的工程副总裁，si five 是一家生产 RISC-V 硅处理器的公司，但这次演讲是对 RISC-V 开放式指令集架构(is a)的更一般的介绍，以及为什么您会关注它。对后者的简短回答和你关心任何其他开放标准的原因是一样的:它促进了互操作性、可重用的工具链，并将导致我们所有人都可以使用更好更快的 CPU。](https://www.youtube.com/watch?v=vCG5_nxm2G4)

视频嵌在下面，绝对值得一看。不幸的是，视频丢失了前几分钟，你可以[跟随她的幻灯片](https://hackaday.com/wp-content/uploads/2020/01/Megan-Wachs-RISC-V-and-FPGAs_-Open-Source-Hardware-Hacking.pdf) (PDF)并阅读我们下面的视频孔中的简要回顾。

 [https://www.youtube.com/embed/vCG5_nxm2G4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/vCG5_nxm2G4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



Wachs 博士首先定义了 ISA:它本质上是描述计算机所说的所有单词的字典。例如，当你用你最喜欢的编程语言编写`a + b = c`时，编译器会把它转换成汇编代码(`add a5, a5, a4`，然后汇编代码会变成 CPU 机器代码的二进制位。ISA 涵盖了汇编语言和机器语言，定义了所有可能的操作，它们接受什么参数，以及它们将结果存储在哪个寄存器或更远的内存位置。

[![](img/825cbd5a6cfd761eceebaeb9cc116e12.png)](https://hackaday.com/wp-content/uploads/2020/01/embedded_riscv.png) 一个普通的 ISA 是一件大事。x86 和 ARM CPU 以完全不同的方式将数字相加，这意味着您需要不同的编译器、汇编器和调试器来处理您的代码，具体取决于您的目标芯片。但它从那里扩散开来。硬件模拟器、可视化工具、文档和底层生态系统中的所有东西都需要根据 CPU 的架构进行定制。如果你想一想所有的专有 isa，这些 isa 以前都有过，相互竞争，现在都没有了(VAX、安腾、SPARC 等等)，那么很多努力都白费了。展望未来，随着越来越多的组件集成到片上系统(SOC)中，仅仅为了对系统进行编程就需要一打 isa 并非不可能。Wachs 博士提到了 NVIDIA Tegra SoC，它具有多个用于声音和音频的 DSP 单元、一个视频编码器、两个 CPU、一个图形处理器、显示驱动程序、一个 USB 外设等。在船上，每个都有独特的软件栈。

RISC-V(“风险五”)，最初是伯克利的一个学生项目，用本质上最简单的开放 ISA 设计解决了这个问题。精简的 RISC-V CPU 可以教授给本科生，但它也足够模块化，如果你喜欢，你可以包括硬件乘法器和其他优化。只要你坚持 ISA 标准，你就能为你的设计准备好编译器、调试器和软件生态系统的其余部分。

随着大量 RISC-V FPGA 内核的出现，这不仅仅是一个学术命题。你，是的，你，可以在一个周末玩真正的 CPU 设计，而且不需要太多的财政支出。为了说明这一点，【Wachs 博士的每个听众脖子上挂着的徽章里面运行着不止一个而是两个 RISC-V CPU。我们已经看到更小、更便宜的 FPGA 开发板也符合要求。当然，有一个学习曲线，但爬上它从来没有这么容易。

开放式硬件设计对于安全性、低功耗应用、削减成本、研究以及一般的黑客攻击都很重要。Wachs 博士演讲的最后三分之一致力于你可能想要使用、调整和构建 RISC-V 环境的方法。当然，开放标准也让大公司的事情变得更加顺利，这意味着你将会看到越来越多的微控制器，甚至是运行在 RISC-V 上的桌面 CPU:与你的开源软件配套的开放标准硬件。但是如果你想更深入地研究，RISC-V 的最大好处实际上是黑客们的。过去，玩 CPU 设计对小男孩或女孩来说是不可能的，但现在已经触手可及。[观看 Supercon 主题演讲](https://www.youtube.com/watch?v=vCG5_nxm2G4)，看看你是否没有得到启发。

## megan wachs 在 supercop 的采访

在她的主题演讲之后，Wachs 博士在 badge hacking 区域花了一些时间讨论她在 SiFive 从 ISA 到生产芯片的工作:

 [https://www.youtube.com/embed/fIsEp4vNJcY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/fIsEp4vNJcY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

