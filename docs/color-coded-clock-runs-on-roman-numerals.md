# 彩色编码时钟运行在罗马数字上

> 原文：<https://hackaday.com/2019/12/24/color-coded-clock-runs-on-roman-numerals/>

按照现代标准，罗马数字有点不寻常。由于同时使用 5 和 10 的名称，并且不能很好地扩展到更高的数字，它们在一些特定的用途之外已经失宠了。其中之一是计时，许多钟表使用古典数字，而不是更流行的阿拉伯数字。[Nicola]的时钟也是如此，尽管是以一种相当不寻常的方式。

![](img/6b28626fc18b2285c0b00daaeefafd29.png)

A diagram of the clock displaying the times 18:40 and 23:04.

建造始于人造霓虹灯棕榈树 LED 装饰，它被掏空并重新安装了由 Arduino Nano 运行的 WS2812B LED 灯条。RTC 用于保持准确的时间，通过运行一次性程序初始化时钟来设置时间。

为了显示时间，发光二极管是彩色编码的。然而，不是使用许多人可能会觉得不熟悉的二进制表示，而是选择颜色来对应罗马数字。选择蓝色、绿色、红色和黄色分别代表 1、5、10 和 50，或者 I、V、X 和 L。Github 为好奇者提供了更多细节。时钟使用 24 小时制，我们认为我们已经弄清楚了显示屏是如何工作的——左边是小时，右边是分钟。

看到一款 LED 时钟与通常的主题有所不同，这很有趣。这些年来，我们已经看到了很多，从[字节钟](https://hackaday.com/2017/06/15/new-take-on-the-binary-clock/)到[这个令人惊叹的闪光灯。](https://hackaday.com/2019/11/24/keeping-time-with-blinkenlights/)如果你已经制作了自己的特殊时计，[一定要让我们知道。](http://hackaday.com/submit-a-tip)