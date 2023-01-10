# calciano 是一个 arduino 计算器

> 原文：<https://hackaday.com/2020/06/28/calcuino-is-an-arduino-calculator/>

基于 Arduino 的计算器本身并不一定非常新颖。然而， *Volos Projects* 的【Danko Bertovi】有一个很好的板，当然，[看起来像一个计算器。](https://www.youtube.com/watch?v=AXu9Mrq3AEk)有 16 个键和一个 LED 显示屏。但是在我们看来，真正的价值是将它作为其他项目的基础。

作为一种廉价的开发板，拥有一个带键盘和显示器的简单处理器非常方便。还有一些额外的 I/O 引脚，例如，下面视频中的第一个例子显示了如何将该设置用作一个简单的风琴。我们希望看到一个用 LCD 取代 LED 的选项，甚至可能还有一些不同的 CPU 选项。

该板本质上是一个 Arduino，带有标准 USB 转串行芯片和 MAX7219 显示驱动器。当然，你可以把所有这些东西放在试验板上，但是看起来不会那么整洁。键盘的一个不寻常之处是它没有多路复用。每个按钮都有一个标签，指示它连接的 Arduino 引脚。因此，键 6 连接到引脚 6，引脚 A2 连接到标有=/A2 的键。

随着廉价 PC 板的出现，我们看到了许多很好的设计，这些设计很容易用于其他用途。例如，我们认为这个主板可以轻松运行 [Kim Uno](https://hackaday.com/2014/11/07/the-kim-1-computer-minified/) ，只需对 I/O 例程进行一些修改。也许甚至能设计出一台更老的电脑的[克隆版来安装在主板上。](https://hackaday.com/2011/09/30/recreating-the-first-pc/)

 [https://www.youtube.com/embed/AXu9Mrq3AEk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/AXu9Mrq3AEk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

