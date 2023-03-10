# (摆脱)LED 中的幽灵

> 原文：<https://hackaday.com/2021/12/08/getting-rid-of-the-ghost-in-the-led/>

多路复用是一种非常古老的技术，其中为了能够控制比控制信号更多的设备，控制信号被混合。对于[mihai.cuciuc]，[来说，当他复用一些非常高效的 led](https://hackaday.io/project/182520-deghosting-multiplexed-leds/details)时，问题就开始了。

问题？在两组各六个 led 中，*连接到一个 Arduino 引脚的两个*led 都将点亮，即使只有一组在接地侧打开。打开的灯组中的 LED 亮着，而其对应的灯组中关闭的*的 LED*也会非常暗。[mihai]能够确定问题不是由于晶体管泄漏，而是由于 led 本身的质量。

除了二极管，什么是 LED？众所周知，二极管也有电容。事实上，这种特性在变容二极管中得到了利用，变容二极管是一种特殊的二极管，其电容可以通过改变阴极上的电压来改变。[mihai]推断这个电容导致电流在关闭的存储体中流动。水流往哪里去了？从打开的 Arduino 引脚，通过其连接的 LED，然后进入*其余的 LED 组*，像电容器一样给它们充电。[mihai]以前没有见过这种情况，但从理论上讲，对于最新一批高效 LED 来说，这种微小的电流足以点亮电流流经的 LED。

[mihai]的解决方案是一个优雅的技巧，他[提供给你阅读](https://hackaday.io/project/182520-deghosting-multiplexed-leds/details)。你可能也会喜欢这个由 w2ew 撰写的[二极管基础介绍。如果你自己有什么很棒的二极管或 LED，一定要](https://hackaday.com/2019/11/11/diode-basics-by-w2aew/)[给我们写信](https://hackaday.com/submit-a-tip/)！