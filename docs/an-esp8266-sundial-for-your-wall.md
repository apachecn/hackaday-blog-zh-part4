# 为您的墙壁安装一个 ESP8266 日晷

> 原文：<https://hackaday.com/2019/03/20/an-esp8266-sundial-for-your-wall/>

黑客绝对喜欢建造时钟。说真的，很少有其他设备有如此多的变化。但是，尽管黑客制造的时钟可能会以二进制形式闪烁显示时间，或者以文字形式显示时间，但它们通常没有指针。显然，在 2019 年，阅读二进制比知道“小手”应该指向哪个方向更合理。

[![](img/49695b06ad2adf945bb163f9b49c6894.png)](https://hackaday.com/wp-content/uploads/2019/03/espdial_detail.jpg) 这个[来自](https://github.com/dheera/shadow-clock)的 ESP8266 供电的“影子时钟”在技术上完整地保留了这一传统，但也仅仅如此。他的时钟没有物理指针，但它使用了一条 RGB LEDs 来投射多色阴影，具有相同的功能。有了他的时钟，你甚至不用试着去找出哪只手是大的，因为它们都一样长。这就是我们所说的进步。

除了挂在墙上看起来有多好之外，这个钟最大的惊喜可能是，制作你自己的版本只需要很少的工作。这是因为[Dheera]特别开始设计比他以前看到的更便宜、更容易制造的东西，我们认为他在很大程度上实现了这个目标。您所需要的只是 3D 打印组件、一个 ESP8266 板和一条 144 个 WS2812B LEDs。

该项目的软件方面也同样简单，您所需要做的就是插入您的 WiFi 网络凭证，让 ESP 从 NTP 获取当前时间。如果你愿意的话，他的源代码将是一个很好的基础，可以用来实现额外的特性，比如整点的动画。

[与 2009 年](https://hackaday.com/2009/12/10/bulbdial-clock-kit-released/)推出的球形钟相比，这些项目在过去十年中变得如此简单，令人难以置信。如今，黑客和制造商可以获得各种工具和组件，这是打造令人惊叹的东西的最佳时机。