# 短导线将 STM32 微控制器变成足够好的无线 UART Blaster

> 原文：<https://hackaday.com/2018/10/29/short-length-of-wire-turns-stm32-microcontroller-into-good-enough-wireless-uart-blaster/>

Hackaday regular [befinitiv]在提示行中写道，让我们知道一个你可能喜欢的黑客，[无线 UART 输出来自一个裸露的 STM32 微控制器](https://befinitiv.wordpress.com/2018/10/25/wireless-uart-with-nothing-but-a-microcontroller/)。渴望完整的 printf 调试体验，但受到可用空间和费用的限制，[befinitiv]受到一个类似黑客的启发，使用 STM32 通过标准 FM 频率发送莫尔斯码。

在这种情况下，[befinitiv]的解决方案更有用，也更合法，因为该软件使用 27 MHz ISM 频段，通过连接到微控制器引脚之一的简单有线天线发射 ASK 调制串行数据。然后，广播可以被 RTL-SDR 接收器接收，并由 GNU Radio 解释为数据流。

STM32 和 GNU Radio Companion graph [的软件都可以在 Bitbucket](https://bitbucket.org/befi/wuart) 上获得。这篇博客文章详细解释了发射机是如何工作的，以及所有 GNU 无线电组件是如何从以太网获取串行数据的。

【封面图片 cc by-sa 由 [Adam Greig，randomskk 在 Flickr 上授权](https://www.flickr.com/photos/randomskk/2637802744)