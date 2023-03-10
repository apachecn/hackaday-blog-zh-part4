# NABU 个人电脑 CPU 升级，模仿 TRS-80

> 原文：<https://hackaday.com/2023/01/01/nabu-pc-gets-cpu-upgrade-emulates-a-trs-80/>

几周前，NABU 的个人电脑在逆向计算界引起了一点轰动。毕竟，在易贝突然出现一大批 20 世纪 80 年代的全新电脑并不常见。开箱后，计算机本身并没有那么有用:没有内部存储，也没有任何应用软件，它实际上只能充当一个基本的开发平台。但由于它的硬件与其他当代家用电脑非常相似，模仿其中一台应该不会太困难，这正是[Ted Fried]所做的:他通过使用他的 MCLZ8 CPU 模拟器，成功地将他的 NABU 变成了 TRS-80 的克隆体。

MCLZ8 基本上是一个 800 MHz 的 Teensy CPU，带有一个适配器板，允许它插入 Z80 插座。它实时模拟 Z80 CPU，但它也持有 TRS-80 ROM，并执行外设之间的实时翻译。在输入端，它读出来自 NABU 8251 a UART 的 ASCII 字符，并把它们存储在虚拟的 TRS-80 的键盘缓冲区中。在输出端，它将 TRS-80 的视频数据传输到 NABU 的 TMS9918 视频芯片。

[![The motherboard of a NABU PC with a Teensy-based CPU upgrade](img/e4af51e12a0cebee03992e9946af820d.png)](https://hackaday.com/wp-content/uploads/2022/12/NABU-MCLZ8-mainboard.jpg) 泰德遇到的一个问题是屏幕分辨率的差异:NABU 的屏幕分辨率为 40×24 字符，而 TRS-80 的屏幕分辨率为 64×16 字符。[Ted]通过简单地将 NABU 标志一直保持在屏幕上解决了垂直差异，并决定忽略掉右边的 24 个字符——无论如何，这对一个典型的 BASIC 程序来说不是一个大问题。

重新设计的 NABU 可能不是一个完美的 TRS-80 克隆体，但这不是重点:它表明 NABU 的硬件可以很容易地被重新编程来做其他事情。例如，[Ted]已经开始了一个新项目的工作，这个项目不模仿 Z80，而是直接在 Teensy 的 ARM A9 处理器上运行代码。正如你可能想象的那样，这使 NABU 的处理能力提高了几个数量级，尽管这种做法的实际用途有限，因为 CPU 仍然需要等待 NABU 的慢速数据总线和显示芯片。[Ted]在下面嵌入的视频中解释了设置并运行了几个令人印象深刻的演示。

[Ted]的 NABU 实验是 Teensy 板灵活性的一个很好的例子:我们已经看到它是如何模仿 Z80 和 8088 的。我们也很好奇其他人会用[NABU 的硬件](https://hackaday.com/2022/11/28/nabu-pc-a-1984-z-80-computer-you-can-buy-today/)——[开发什么，当然，如果他们还能买](https://hackaday.com/2022/12/02/hackaday-podcast-195-no-nabu-for-you-self-assembling-3d-prints-black-hats-look-at-ev-chargers/)的话。

 [https://www.youtube.com/embed/wxjQhCCRSP0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/wxjQhCCRSP0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

