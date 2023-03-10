# (可能是)对 SAM D21 MCU 注释最彻底的链接器脚本

> 原文：<https://hackaday.com/2021/01/19/the-probably-most-thoroughly-commented-linker-script-for-the-sam-d21-mcu/>

链接器脚本是那些做软件开发的人都不想处理的事情之一，但是像生活中的许多事情一样，有时它们是不可避免的。尽管人们可以继续假装链接器脚本不存在，让 ide 处理这些讨厌的细节，但我们中的一些人患有这种叫做“好奇心”的不幸疾病，并且必须知道。像[西娅]这样的人。

最近，[Thea] [写了一篇博客文章](https://blog.thea.codes/the-most-thoroughly-commented-linker-script/)，详细介绍了微芯片 IDE 为基于 Cortex-M 的 SAM D21 项目生成的链接器脚本的功能。其结果是一个很好的注释文件内容的概述，伴随着链接到 Arm 和 GCC 文档以及其他适当的参考。整个链接器脚本(。ld 文件)可以在 GitHub 上查看[。由于 SAM D21 是 Arduino 和 Arduino 兼容板的流行选择，本文是理解链接器脚本的作用以及它如何影响项目的良好起点。](https://github.com/theacodes/Winterbloom_Castor_and_Pollux/blob/master/firmware/scripts/samd21g18a.ld)

对于其他(Cortex-M)MCU，这个链接器脚本也是一个有用的起点。尤其是了解哪些部分是必需的，以及更改它们会对最终(ELF)二进制文件和最终写入 MCU 的固件产生什么影响。我们[最近还讨论了 Cortex-M](https://hackaday.com/2020/12/23/bare-metal-stm32-exploring-memory-mapped-i-o-and-linker-scripts/) 的链接器脚本，以及内存映射 I/O 的概念。