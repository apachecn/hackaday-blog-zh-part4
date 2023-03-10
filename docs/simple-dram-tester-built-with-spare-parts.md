# 用备件构建的简单 DRAM 测试器

> 原文：<https://hackaday.com/2022/02/27/simple-dram-tester-built-with-spare-parts/>

一些最受欢迎的老式电脑现在已经超过 40 岁了，它们的内存也不如以前了。识别坏的内存芯片会很快变成一件苦差事，所以[Jan Beta]花了一些时间用备件组装了一个便宜的 DRAM 测试器。

这个小测试器可以配合 4164 和 41256 DRAM 内存芯片使用。在 20 世纪 70 年代和 80 年代，4164 DRAM 被用于几款流行的家用电脑，包括 Apple ][系列、Commodore 64、ZX Spectrum 等等。同样，41256 也用于海军准将阿米加号。这些计算机在老式计算社区中非常受欢迎，在其中任何一台计算机中发现糟糕的内存都是很常见的。

这个 DRAM 测试器以 Arduino 为核心，使用最基本的电子元件，任何一个普通的修补者都应该有几乎所有的存货。[原始项目可以在这里找到](https://forum.defence-force.org/viewtopic.php?t=1699)，包括 Arduino 代码。只需将可疑芯片插入 ZIF 插座，按下重置开关，然后等待 LED 灯亮起——绿色表示正常，红色表示没电了。

当你深陷可疑的梦境时，这是一个很好的理智检查。失败的测试是芯片坏了的明确信号，然而测试者偶尔会报告错误的通过。不是每一个问题都可以用这样一个简单的测试器来识别，但是它可以很好地剔除那些绝对没有用的芯片。

如果你不缺钱，那么 [Chip Tester Pro](https://hackaday.com/2021/10/23/chip-tester-knows-if-your-old-chips-are-working/) 可能更合你的意，然而，用备件构建你自己的简单测试器的简单和节俭是无可匹敌的。如果你有点冒险精神，这个[在线调试器](https://hackaday.com/2021/12/30/customisable-micro-coded-controller-helps-with-in-circuit-debugging/)可能会派上用场。

 [https://www.youtube.com/embed/vu1iFCjZZjo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/vu1iFCjZZjo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

