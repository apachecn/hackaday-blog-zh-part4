# 带有柔和背光的自定义宏键盘

> 原文：<https://hackaday.com/2022/04/07/custom-macro-keyboard-with-sweet-backlighting/>

从那些没有桌面空间的最小的 60%键盘到那些整天做数据输入的带数字键盘的键盘，几乎每个人都有适合的键盘尺寸和形状。唯一的问题是，即使是最大的键盘，它们所能做的仍然相当有限。如果你发现自己想要更多的功能，你可能会想要做一些东西[，比如这个带有内置 LED 背光的定制宏键盘](https://www.kaper.com/electronics/macro-keypad/)。

不同于 Cherry MX 那样的标准机械键盘开关，这款产品基于 TS26-2 按钮，内置 LED 照明。[atkaper]只需要一个按钮来管理 MS Teams 上的静音按钮，但仍然在这个键盘中内置了总共八个开关，它们都可以单独编程，具有不同的功能。控制器是 Arduino Leonardo，外壳是 3D 打印的。

搭配经典的 IBM 型键盘，这种新的宏键盘增加了大量的功能，同时还可以控制 LED 背光。宏键盘非常有用，尤其是它们能够通过控制运行在其上的软件来轻松改变功能。大多数构建的关键是在一些 Atmel 微控制器中发现的 [32U4 芯片，它允许它轻松地将键盘(和鼠标)功能传递给它所插入的任何计算机。](https://hackaday.com/2012/06/29/turning-an-arduino-into-a-usb-keyboard/)