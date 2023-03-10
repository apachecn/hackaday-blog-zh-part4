# AVR 多功能工具学习最新技巧

> 原文：<https://hackaday.com/2020/07/02/avr-multi-tool-learns-the-latest-tricks/>

像我们许多摆弄微控制器的人一样，[Mike]和[Brian]经常发现自己在使用 ISP 编程器和 USB 转串行适配器。但当他们开始研究最新一代的 ATtiny 芯片时，他们发现自己需要一个统一的程序，以及调试接口(UPDI)程序员。所以他们决定[将所有三种功能打包成一个方便的开放硬件小工具](https://wordcraft.com/avrgpp/home.html)。

[![](img/af5e7c7d6f5c3a5b35ffbfdc643e90fe.png)](https://hackaday.com/wp-content/uploads/2020/06/avrgpp_detail.png) 他们称自己的创造为 AVR 通用程序员，简称 AVRgpp。它运行在带有 Pro Mini bootloader 的 ATmega328P 上，这意味着编程器本身与 Arduino IDE 完全兼容。CH330N 提供 USB 转串行功能，MC14053 数字开关 IC 用于选择与 AVRgpp 的板载 MCU 或目标设备通信。

一个 128 x 32 I2C 有机发光二极管和两个按钮用于选择设备的当前模式，还有一个物理开关用于选择目标的 5 V 或 3.3 V 电源。还有一个 ST662 12 V 调节器，因为 UPDI 目标偶尔需要高压脉冲来切换到编程模式。一切都包装在一个口袋大小的激光切割外壳中，你可以很容易地扔在你的包里。

[Mike]和[Brian]说，如果有足够的兴趣，他们正在考虑将 AVRgpp 投入小规模生产，所以让他们知道你是否想得到一个而不必自己建造它。