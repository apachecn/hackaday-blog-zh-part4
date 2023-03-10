# 更上一层楼的 Z80 电脑

> 原文：<https://hackaday.com/2020/02/23/a-z80-computer-at-the-next-level/>

在 8 位家用计算机时代结束时，出现了一些试图弥合 8 位和 16 位世界之间差距的机器，要么通过提供具有向后兼容模式的 16 位设备，要么通过提供具有增强能力的 8 位设备来与其较新的对手竞争。面对新的 16 位平台，这些产品在很大程度上被搁置了，但它们和随后几十年出现的 8 位处理器的各种增强版本提供了一个迷人的机会。这是[Konstantin Dimitrov]在他的 [Z20X 计算机项目中探索的一个主题，](https://z20x.computer/)这是一台使用 Zilog eZ80 处理器的机器，运行频率为 20 MHz，具有 512 kB 的外部存储器，以及一个用于 7”TFT 屏幕模块的接口。

eZ80 是最近开发的一款流水线处理器，能够实现更高的时钟速度和高达 16 MB 的内存寻址，同时保持与 Z80 的软件兼容性。如果它在 20 世纪 80 年代末上市，可能会引起轰动，但它却出现在嵌入式计算机中，也许是黑客读者最感兴趣的，在 TI 的可编程计算器系列中。

Z20X 设计为通孔板，唯一的 SMD 元件是 eZ80 本身。我们可以理解这背后的动机，但同时想知道它在 2020 年可能的建造者是否会是对 SMD 组装无动于衷的人。它有一个处理器模块系统，以备将来升级，还有一个扩展背板，可以选择 RC2014 兼容总线。还有 PS/2 键盘和鼠标连接器、串行总线和板载声音芯片。该网站缺乏任何软件的细节，但我们希望它能与典型的 Z80 逆向计算机产品一起工作，如基本的解释程序和 CP/M 操作系统。

这台机器可能会吸引逆向计算爱好者，但如果它在十年前出现，即使没有显示器，它无疑也会成为人们渴望的对象。然而，它确实提醒我们 Z80 系列已经更新，尽管我们大多数人都会继续前进，但它仍然提供了一些可能感兴趣的芯片。同时，为了进行比较，看看去年对 RC2014 retrocomputer 板系列的最新产品[的评测。](https://hackaday.com/2019/10/02/review-the-rc2014-micro-single-board-z80-retrocomputer/)

谢谢你的提示。