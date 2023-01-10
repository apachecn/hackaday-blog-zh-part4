# 串行西多会数字模块

> 原文：<https://hackaday.com/2022/12/12/serial-cistercian-digit-module/>

毫无疑问，7 段显示屏是显示发光数字的黄金标准。但是回到一个更古老的显示数字的系统——西多会怎么样？用 31 个 0805 LEDs，[Josue Alejandro]制作了一个简单的模块，显示一个西多会数字(0-9999 之间的任何数字)。

第一次迭代使用了堞形边缘，并需要大量的 GPIO，因此在下一个版本中，他切换到从 Lumissil (IS31FL3726A)转换而来的串行到并行。一个扩散器和间隔器是由 PLA 印刷而成的，看起来非常时髦。

当然，它不能就此止步，第三次修订使用了 SK6812 Neopixels，允许完整的 RGB 功能。所有的设计文档、布局文件和极其详细的图纸[都可以在 GitHub](https://github.com/JosueAGtz/CistercianDisplay) 上获得。让这变得非常方便的是拥有一个可以轻松添加到项目中的模块。甚至可能作为[中的一个组件，一个盒子](https://hackaday.com/2021/03/19/planetary-escape-room-in-a-box/)中的密室，它可以让你闪现多个数字。或者也许[是一个时尚的时钟](https://hackaday.com/2021/03/29/oh-brother-would-you-look-at-this-cistercian-clock/)。我们甚至向某人挑战，通过将这些模块[与这个键盘](https://hackaday.com/2022/05/10/number-like-its-1234-ad-with-this-cistercian-keypad/)结合起来，创造出一个计算器。