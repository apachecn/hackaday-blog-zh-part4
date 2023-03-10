# RISC-V:为什么 ISA 之战还没有结束

> 原文：<https://hackaday.com/2019/11/12/risc-v-why-the-isa-battles-arent-over-yet/>

计算机处理器使用一种所谓的指令集架构来与自身电路之外的世界交流。这个 ISA 由许多指令组成，这些指令本质上定义了处理器的功能，这解释了为什么今天仍然存在如此多的 ISA。毕竟，很难找到一个能为尽可能多的不同用例工作的 ISA。

一个相当新的 ISA 是 RISC-V，它的第一个版本是 2010 年在加州大学伯克利分校创建的。它旨在成为一个完全开放的 ISA，面向学生(作为一种学习工具)和工业用户，据称它包含了许多设计选择，这将使它对许多应用程序更具吸引力。

在这篇文章中，我将看看背后的营销，以评估 RISC-V 究竟如何不同于其他开放的 isa，包括电源，SPARC 和 MIPS。

## 欢迎来到 RISC 的世界

精简指令集计算机( [RISC](https://en.wikipedia.org/wiki/Reduced_instruction_set_computer) )是一种专注于创建只需要有限数量的处理器周期来执行单个指令的指令集的 is a。理想情况下，一条指令正好需要一个周期。这与复杂指令集计算机( [CISC](https://en.wikipedia.org/wiki/Complex_instruction_set_computer) )形成对比，后者专注于减少应用程序所需的指令数量，从而降低代码存储需求。

如今，CISC 基本上已经不复存在，摩托罗拉 m68k ISA 已被搁置，任何基于英特尔 x86 CISC ISA 和后续产品(如 AMD 的 64 位扩展)的 CPU 在内部都是一个 RISC 处理器，带有 CISC ISA 解码器前端，可将 CISC 指令分解为 RISC 指令(微操作码)供其 CPU 内核使用。至少就 CISC 对 RISC ISA 的战争而言，我们可以说 RISC 肯定赢了。

## 多种风格的 RISC

虽然 RISC ISA 如[阿尔法](https://en.wikipedia.org/wiki/DEC_Alpha)和 [PA-RISC](https://en.wikipedia.org/wiki/PA-RISC) 由于公司政策而不是 ISA 设计本身的任何不足而不幸消亡，但幸运的是，我们今天仍然有一个健康的 RISC ISA 集合，最值得注意的是:

*   [SuperH](https://en.wikipedia.org/wiki/SuperH) (带开放 J-2 实现)。
*   [ARM](https://en.wikipedia.org/wiki/ARM_architecture) (完全专有)
*   MIPS (开放，免版税)
*   [权力](https://en.wikipedia.org/wiki/Power_ISA)(开放，免版税)
*   AVR (专有)
*   [SPARC](https://en.wikipedia.org/wiki/SPARC) (开放，免版税)
*   OpenRISC (开放，免版税)

RISC-V 作为一个新来者，将其 9 年的(学术)发展与 MIPS 的 34 年以上、SPARC 的 33 年以上以及 IBM 早在 20 世纪 70 年代早期就开始开发的 Power ISA 相比较。考虑到围绕这个新 ISA 的大肆宣传，它肯定有一些不同之处。

这也是考虑到 OpenRISC，它在 2000 年开发时有许多与 RISC-V 相同的目标，尽管它已经投入商业使用，但从未引起多大轰动。

## 变化的风景

值得注意的是，早在 2010 年 RISC-V 开发的时候，SPARC 已经是一个开放的 ISA 很长一段时间了，欧空局的[莱昂](https://en.wikipedia.org/wiki/LEON) SPARC 在 VHDL 中的实现从 1997 年就开始了。自 2010 年以来，MIPS 和 IBM 的 Power ISA 也加入了开放和免版税 ISA 的行列，提供 Verilog、VHDL 和其他语言的开源设计。自 20 世纪 90 年代以来，MIPS 一直是处理器 isa 的标准教学工具(通常基于 [DLX](https://en.wikipedia.org/wiki/DLX) )，许多学生编写自己的极简 MIPS 内核作为课程的一部分。

由于在这些领域中存在竞争者，RISC-V 不能简单地通过开放、免版税、拥有更成熟的 ISA 或更好的免费 HDL 内核来区分自己。相反，它的 ISA 必须具有从能效或其他指标的角度看具有吸引力的功能，使其能够比竞争对手更有效或更快地处理数据。

这里的一个定义特征是 RISC-V ISA 不是一个单一的 ISA，而是超过 20 个独立的 ISA，每个 ISA 专注于一组特定的功能，例如位操作、用户级中断、原子指令、单精度和双精度浮点、整数乘法和除法等等。RISC-V 生态系统中另一个有趣的地方是，我们鼓励在没有任何批准过程的情况下添加定制指令集。

## 忽视未来

RISC-V ISA 本身的一个有趣的选择是子例程调用和条件，RISC-V 没有提供条件码寄存器([状态寄存器](https://en.wikipedia.org/wiki/Status_register))或进位位。这种选择使得[预测](https://en.wikipedia.org/wiki/Predication_%28computer_architecture%29)不可能，而是迫使处理器执行每一个分支，期望其中一个是正确的，丢弃其他分支的结果。由于分支预测在 RISC-V 中是可选的，这可能会带来巨大的性能和能源成本损失。

由于其他主要架构都使用谓词来提高性能，特别是对于较短跳转的块，例如由大的 if/else 块或 switch 语句产生的块，所以忽略这个特性是相当大胆的。RISC-V 开发人员提供的设计原理是，快速、无序的 CPU 可以通过强力处理来克服这一限制。有趣的是，尽管他们为自己的紧凑指令通常非常紧凑而自豪，但他们并不认为没有谓词的代码会产生更大的代码长度是一个问题。

在这里，RISC-V 开发过程有点精神分裂的性质开始显露出来。虽然它应该很适合嵌入式，可能是低时钟处理器，但与基于 ARM 的等效微控制器相比，它缺乏预测性可能会损害它的原始性能，其 Thumb-2 compact 指令集也比 RISC-V compact ISA 更有效。

## RISC-V 选择不确定性而非确定性

在这一点上，RISC-V ISA 唯一被“冻结”的部分是 32 位和 64 位版本的基本整数集，以及整数乘法和除法、原子、单精度和双精度浮点以及四精度浮点和压缩指令的扩展。

虚拟机管理程序、位操作、事务内存和用户级中断等扩展仍在不断变化，因此除了实验性使用之外不适合任何东西，这进一步分裂了整个 RISC-V 生态系统。这清楚地表明，RISC-V 不是一个“完成”的 ISA，但仍然处于开发的早期阶段。虽然它的核心是可用的，但嵌入式指令集也没有完成，而且没有现成的性能数据来支持它可以轻松胜过任何竞争对手的说法。

更糟糕的是，RISC-V 可用的 HDL 内核和软件工具可能还不成熟。随着 ISA 集的稳定化需要时间，很少有内核和工具提供或期望基本(RV32I 或 RV64I)功能之外的任何东西也就不足为奇了。由于没有更多的指令集被完成并被集成到芯片中，对于一个旁观者来说，有一个有趣的想法，也许 RISC-V 对这场新的 ISA 战争的主要贡献并不是 RISC-V 一定更优越，或者它甚至没有任何长期的商业可行性。

## 展示如何去做

早在 2000 年，当 OpenRISC 项目启动时，市场似乎对开放和免费的 ISAs 以及相关的处理器设计没有太大的兴趣。今天，这似乎是完全不同的，是 RISC-V，而不是 OpenRISC 引发了这种企业思维的变化，导致 IBM 在有限的程度上开放了其 Power ISA，以及 MIPS ISA 和[甚至 ARM ISA](https://staceyoniot.com/why-arm-opened-up-its-instruction-set-and-what-it-means-for-iot/) 。RISC-V 有 DARPA 的资助，而 OpenRISC 可能没有在这里发挥作用，但是谁在计算呢？

不管这些细节如何，计算机硬件行业似乎已经走上了一条新的道路，在这条道路上，即使是一个业余爱好者也可以获得许多支持良好的 HDL 内核，并可以自由地试验 ISA。现在，人们可以在完全开放的 MIPS、SPARC、Power、RISC-V 和 SuperH 内核之间进行选择，也许有一天完全开放的 ARM 内核也会成为现实。

在某种程度上，它让人回想起 20 世纪 80 年代，当时在快速增长的家用电脑市场中，多家 CPU 制造商努力让他们的 ISA 和芯片成为最受欢迎的产品，Zilog 的 Z80 和 6502 当然是 8 位产品的有力竞争者，然后一个名为“英特尔”的小暴发户开始入侵，最终导致 ISA 多样性在桌面上以及最近在视频控制台上似乎完全消失。

## 为多样性干杯

我不会说我渴望不同平台的日子(以免有人说我是愚蠢的混蛋)。在个人计算机发展的年代，任何在软件行业工作的人都会发现自己在经历在 Commodore 64 和 ZX 频谱之间移植软件的痛苦记忆。认为我们现在过得好得多并不是一个极端的立场。

也就是说，每个对竞争意味着什么有所了解的人都可以看到，一个只有英特尔、只有 AMD、只有 ARM 或只有 RISC-V 处理器的世界将会非常乏味。正是思想的碰撞，差异的比较，让人们不断思考，不断创新。现代软件实践应该意味着跨平台兼容性不再像 20 世纪 80 年代和 90 年代那样是个大问题。

在 ISAs 的世界里，这是一个开放的、多样化的未来。