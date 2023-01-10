# BCD 到 I2C:把谢妮柜台变成你想要的样子

> 原文：<https://hackaday.com/2020/03/28/bcd-to-i2c-turning-a-counter-into-whatever-you-want-it-to-be/>

每当一个项目需要显示数字时，7 段显示器是经典而直接的选择。然而，如果你更喜欢乡村、复古、近乎神秘和蒸汽的外观和感觉，那就很难打败 Nixie 管温暖的橙色光芒。曾经注定作为过时的技术，它们已经在业余爱好者的空间中恢复了它们的意义，并成为如此频繁和故意的设计选择，以至于很容易忘记旧设备实际上是出于缺乏替代方案的需要而使用它们。证据 A:在阁楼发现的脉冲计数器【soldeerridder】被他变成了一个通用的 I2C 控制显示器。

[soldeerridder]并不只是抢救谢妮电子管，而是保留并重新使用原始设备，目标是嵌入英特尔 Edison 模块并通过 I2C 连接。自然，由于计数器是一个独立的设备，主要包含少量的 SN74141 驱动程序和 SN7490 BCD 计数器，因此没有现成的 I2C 连接。与此同时，Edison 无论如何都会取代 7490s 的功能，因此解决方案既简单又天才:移除 BCD 计数器 IC，并设计一个包含 PCF8574 GPIO 扩展器的定制 PCB，作为它们的替代产品，从而允许通过 I2C 向驱动器 IC 发送任意值，同时保持其他一切的原始形状。

包含六个谢妮电子管，显而易见的选择当然是[把它当作时钟](https://hackaday.com/tag/nixie-clock/)，但是【soldeerridder】想要的不止这些。好的，*会在[的项目博客](https://www.element14.com/community/community/design-challenges/upcycleit/blog/2017/04/03/upcycle-it-nixie-display-index)上显示时间和日期，还有一些传感器值，甚至类似的东西。如果你想自己尝试谢妮电子管，但缺乏匹配的设备， [Arduino 显然可以满足你的需求](https://hackaday.com/2019/04/04/arduino-shield-makes-driving-nixies-easy/)。尽管如此，你还是不妨[走另一个方向](https://hackaday.com/2019/10/30/multimeter-display-perked-up-with-nixies-leds-and-neon-tubes/)吧。*

 [https://www.youtube.com/embed/rpa0qwml7mU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/rpa0qwml7mU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

