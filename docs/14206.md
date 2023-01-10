# 是 Linux。在 ESP32 上

> 原文：<https://hackaday.com/2022/07/14/its-linux-on-an-esp32/>

按照今天的标准，运行一个基于 Linux 的操作系统在内存和处理器能力方面的需求少得惊人。过去，我们在英特尔 386 和 486 机器上运行早期的 Linux 版本，与我们今天使用的数千兆字节的众核处理器相比，内存量非常小。

因此，许多功能更强大的微控制器也应该运行 Linux，这是显而易见的，但当然，由于缺少内存管理单元，它们通常无法运行 Linux。最初的 ESP32 就是这样一个候选者，有足够的能力但无法运行 Linux。没那么快，因为[德罗尔·格鲁斯卡]已经设法在 Espressif 的双核芯片上启动了一个 Linux 内核。到底是怎么回事？[通过在其上仿真 RISC-V 处理器并引导内核的 RISC-V 版本](https://blog.drorgluska.com/2022/07/risc-v-linux-on-esp32.html)。

有问题的仿真器是[Fabrice Belard]的 [TinyEMU](https://bellard.org/tinyemu/) ，这是一款将 RISC-V 和 x86 带到有限规格平台的软件，文章描述了对 ESP32 瓶颈的广泛优化和跟踪，最终能够在 1 分 35 秒内启动 Linux 内核。当然，这只是一个证明可以做到的练习，我们不会很快看到基于 Linux 的 ESP 项目，但这仍然是一项令人印象深刻的工作。

这不是我们见过的运行 Linux 的最低规格微控制器，[早在 2012 年，我们就在运行 8 位 AVR](https://hackaday.com/2012/03/28/building-the-worst-linux-pc-ever/) 的仿真 ARM 上见过它。