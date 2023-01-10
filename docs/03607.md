# 为 STM32 G0 系列构建开发板

> 原文：<https://hackaday.com/2019/07/16/building-a-development-board-for-the-stm32-g0-series/>

当[安迪·布朗]最近被 ST 的新 G0 系列 MCU 绊倒时，他在经过一些研究后发现，了解 STM32G0xx 所有知识的最好方法是[基于 STM32G081 制作自己的开发板](http://andybrown.me.uk/2019/07/08/stm32g081dev/)。其结果是一个 Nucleo 风格的板，将所有引脚分为方便的 2.54 mm 接头，并具有许多细节，如板载硬币电池和用于 RTC 的 32.768 kHz LSE 振荡器，以及用于 MCU 的三种不同电源(3.3 V、2.5 V 和 1.8 V)。

该板由一个外部 ST-Link 编程器编程，该编程器连接到 MCU 上的 SWD 接口，并提供一个 20 引脚编程接头。虽然绝不是小或紧凑，但它非常容易进行试验板和原型制作，所有 2.54 毫米接头都可以从底部和顶部接触到。

至于 STM32G0 系列本身，与 F0 相比，其性能仍有待评判。前者将 Cortex-M0 内核替换为 M0+，流水线长度缩短(G0 中的 3 个阶段)，但频率提高(64 MHz 对 48 MHz)。G0 的 SRAM 稍微多一点，但目前为止闪存存储较少。根据 ARM 的说法，该 MCU 系列旨在消除仍然使用 8 位 MCU 的任何需要。确实是大索赔。

[Andy]在开发该板时遇到的最大问题可能是 CH340 USB-UART 芯片。像往常一样，从全球速卖通订购 CH340G ICs 在第一次主板修改时就无法工作，这迫使他改用 CH340E，并要求重新安装主板。这个版本有一个内部振荡器，并且作为一个额外的奖励，当它到达时，甚至是在原来的磁带包装中，而不是像 CH340G 部件一样在一个塑料袋子中。

休息之后，请观看[Andy]浏览设计的视频。

现在开发板已经启动并运行，看看这种新的 MCU 系列能提供什么样的性能，以及它是否符合宣传的要求，将会很有意思。在[Andy]的博客上，您可以找到设计文件、gerbers 和完整的电路板 BOM，这样您就可以轻松地制作自己的电路板。

 [https://www.youtube.com/embed/v8Xii3Ykvgw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/v8Xii3Ykvgw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

