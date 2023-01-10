# 用于稳定基准的晶体振荡器

> 原文：<https://hackaday.com/2018/07/30/a-crystal-oscillator-for-a-stable-bench-reference/>

[保罗]喜欢一个精确的振荡器。他最近的视频展示了一个带“手表晶体”和 CMOS 计数器的晶体振荡器，CD4060。使用这样的电路可以产生非常稳定的频率，因为 32.768 kHz 晶体是 2 的幂，所以计数器可以产生很好的分频。

我们已经看到了用十进制计数器(如 4518B)除以 10 而不是 2 的幂来制作频率标准的相同技巧。一个 1 MHz 晶振可以轻松产生 100 kHz、10 kHz 等。

[Paul]提到时钟是施密特触发器输入(他说的是输出，但他指的是输入)，因此它可以毫无问题地接受来自振荡器的噪声输入。

该板是商用的，但电路足够简单。4000 系列 CMOS 很好，因为它可以在很宽的电压范围内使用，并且可以在线性范围内偏置，例如简单的晶体振荡器。请注意，如果您确实想将 CMOS 门用作线性器件，您需要寻找[无缓冲版本](http://www.ti.com/lit/an/scha004/scha004.pdf) (UB 后缀)。1972 年，4000A 系列集成电路出现，并且全部无缓冲。然而，有许多缺陷。“B”系列以增加传播延迟为代价修复了其中一些缺陷。通过缓冲。由于一些设计依赖于无缓冲行为，因此某些器件保持无缓冲状态，并带有“UB”后缀。

如果你想重温施密特触发器，我们有。如果你想知道[为什么这些被称为手表水晶](https://hackaday.com/2018/06/07/dive-inside-this-old-quartz-watch/)，我们也可以展示给你看。

 [https://www.youtube.com/embed/Oeliyi1iKGk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Oeliyi1iKGk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

