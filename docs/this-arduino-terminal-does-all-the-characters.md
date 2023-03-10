# 这个 Arduino 终端可以处理所有的字符

> 原文：<https://hackaday.com/2021/10/23/this-arduino-terminal-does-all-the-characters/>

哑终端的工作最初是纸电传打字机的延续，从键盘发送文本，并在屏幕上显示接收到的任何内容。但随着计算机系统的需求超出了单纯的 ASCII 所能提供的范围，它们的功能也随着额外的字符和图形扩展而扩展，我们在今天的 Unicode 字符集，甚至是你手机上的所有表情符号中都可以看到它们的后代。因此，一个功能齐全的终端有许多半图形字符，从中可以产生出人意料的非文本输出。这是[Michael Rule]已经做了一些工作的东西，他的 ILI9341TTY，[是一个 USB 串行终端监视器，使用 Arduino Uno 和 ILI9341 LCD 模块](https://github.com/michaelerule/ILI9341TTY)，支持尽可能多的扩展字符。

[![A graph, entirely in Unicode characters.](img/390cc4a5502780223c23096a15893848.png)](https://hackaday.com/wp-content/uploads/2021/10/ploteg.png)

A graph, entirely in Unicode characters.

公平地说，我们大多数经常使用终端的人都没有超越 ASCII，因为现代终端很可能位于桌面 GUI 之上的窗口中。因此，即使你对硬件终端显示器没什么用，在那些罕见的字符集中仍然可以找到很多有趣的东西。我们最喜欢的可能是代表传统计算的符号，这是一组半图形字符，对于使用过一两台 8 位家用电脑的读者来说可能很熟悉。他提供了一个图表示例，使用了这些带有 ANSI 转义码的字符，这肯定不是您所期望的终端。

如果微控制器终端引起了你的兴趣，[这不是我们带给你的第一个](https://hackaday.com/2019/11/22/a-tiny-terminal-for-your-serial-access-needs/)。