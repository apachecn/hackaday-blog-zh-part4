# 拜拜 486 上的 Linux。我们会想你吗？

> 原文：<https://hackaday.com/2022/11/02/bye-bye-linux-on-the-486-will-we-miss-you/>

本周技术新闻的一个脚注来自 Linus Torvalds，[他在 Linux 内核邮件列表帖子中提出了放弃支持英特尔 80486 架构](https://lkml.iu.edu/hypermail/linux/kernel/2210.2/07782.html)的想法。一个旧的、很少使用的架构可能会被抛弃，这并不奇怪，十年前，同样的命运也降临到了 Linux 的第一个平台 80386 上。486 系列可能在桌面上早已寿终正寝，但由于它们并没有完全从嵌入式领域消失，仍然是复古计算机人群的最爱，因此值得花一分钟来研究一下这一举动可能带来的后果(如果有的话)。

## 486 还是一件东西吗？

[![Block diagram of the ZFx86 SoC](img/5b40ce08dcba7a52d7ce5672e8c252de.png)](https://hackaday.com/wp-content/uploads/2022/10/zfx86-diag.jpg)

An entire 486 PC in a chip that only uses 1W, that would have been amazing in 1994!

英特尔 80486 于 1989 年发布，是其先前 32 位微处理器 80386 系列的改进版本，具有片上高速缓存、更高效的流水线和内置数学协处理器。它有一个 32 位的地址空间，尽管实际上 20 世纪 90 年代 RAM 和主板的限制意味着一个典型的 486 系统将有兆字节数量的 RAM。在其生命周期中，时钟速度有 16 MHz 至 100 MHz 的版本，以及协处理器禁用的低端“SX”范围。它本来是运行 WIndows 3.1 的处理器，也是 Windows 95 的有力平台，但到了 90 年代末，它在桌面上的日子结束了。英特尔将嵌入式处理器系列延续到 2000 年代，最终在 2007 年退出。然而，486 的故事并没有结束，因为在其活跃的一生中，一系列竞争对手已经对 486 产生了自己的看法。非英特尔 486 芯片的寿命超过了原版，即使在 2022 年的今天，也有不止一家公司在生产 486 兼容设备。RDC [生产一系列运行 486 代码](https://www.rdc.com.tw/?route=home/mcu32bit)的 RISC SoCs，根据 ZF 微解决方案网站，他们仍然吹嘘[是 Cyrix 486 系列](http://www.zfmicro.com/zfx86.html)的后代。关于 DM & P 的 [Vortex86](https://www.vortex86.com/) 系列是否也是 486 衍生产品，网上有些混乱，但是我们知道它们是 Rise Technology 的奔腾克隆产品的后代。

## 486 到底能坚持到哪里？

[![An array of 486 chips from different manufacturers.](img/9c4048420e3f553129196f6bbd3d0889.png)](https://hackaday.com/wp-content/uploads/2022/10/486_Prozessoren_von_AMD_Cyrix_IBM_Intel_ST_Texas_Instruments.jpg)

486s and compatible chips were produced by a variety of manufacturers. Winhistory, [Copyrighted free use](https://commons.wikimedia.org/wiki/File:486_Prozessoren_von_AMD_Cyrix_IBM_Intel_ST_Texas_Instruments.jpg).

很可能很少有工程师会在 2022 年为新的 x86 嵌入式设计选择这些器件，尤其是因为市场上有更多采用奔腾或更新内核的设备可供选择。我们在工业应用中的模块上遇到过它们，我们猜测它们仍在生产中，因为在某个地方仍有长期的机器产品线在使用它们。我们非常迷恋 RDC 部分，它是一个完整的 486 PC 芯片，功耗仅为 1 W，因为我们 90 年代的自己会对长电池寿命的手持 486 PC 垂涎三尺，但在 2022 年，我们应该需要快速修复便携式 486 游戏，有很多 ARM 板可以足够快地运行软件仿真器，不会出现任何差异。那么，相对较小的 486 个用户的社区会怀念即将到来的 Linux 内核对他们平台的支持吗？要回答这个问题，有必要考虑一下这些机器可能运行的软件类型。

如果有一件事是工业机器的操作员所重视的，那就是一致性。对他们来说，机器是一个电器而不是一台电脑，它必须连续无误地工作。要做到这一点，它需要一个坚如磐石、稳定的软件基础，而不是一个瞬息万变的软件基础，那么一个过时的工业控制器需要访问最新、最棒的 Linux 发行版吗？我们认为不太可能，事实上我们怀疑过时的基于 x86 的工业控制器更有可能使用 DOS 风格。与此同时，逆向计算人群也更有可能运行 DOS 或 Windows 版本，因此很难想象他们中的许多人会将最新、最棒的产品塞进一台 16 兆内存的 486DX。

## 当你想起你的内存有多少时，记忆的道路就不那么美好了

我尝试的第一个 Linux 是 1994 年某个时候在 486DX-33 上的 Slackware 版本。在那个时候，对于日常操作系统来说，这是一个非常冒险的选择，虽然作为一个实验来说这很棒，但我一直在日常驱动程序中使用 AmigaOS、DOS 和 Windows。大约十年后，有了闪亮的新 Core Duo 笔记本电脑，我会转向永久双启动，并最终完全放弃 Windows，而不是只在服务器上使用 Linux，从那时起，几代 PC 都延续了这一趋势。如果你真的在过去使用过 486，那么很容易认为它仍然是一个竞争者，但是想想在这中间的几年里有多少连续的平台经过我的办公桌，就能明白这个古老的平台到底有多古老。在上面的段落中，我们已经看了一下 486 世界的状态，我们猜测只有极少数人会想念对 486 处理器的支持。你呢，你跑 486 干什么？请在评论中告诉我们。

标题图片:寡头垄断， [CC0](https://commons.wikimedia.org/wiki/File:Intel_i486DX-33.jpg) 。