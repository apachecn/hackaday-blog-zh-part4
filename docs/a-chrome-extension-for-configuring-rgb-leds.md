# 用于配置 RGB LEDs 的 Chrome 扩展

> 原文：<https://hackaday.com/2019/04/28/a-chrome-extension-for-configuring-rgb-leds/>

像我们几乎所有人一样，[安迪·施瓦茨]喜欢 RGB LEDs。具体来说，他喜欢把它们放在遥控车辆上，如飞机上的导航灯或汽车上的闪光灯和前灯。他发现自己经常为这些安装中的每一个重写非常相似的 Arduino 代码，并最终决定通过[创建一个专门用于驱动 RGB LEDs 的可定制 Arduino 固件](https://github.com/flyandi/BitsyLED)来节省自己(以及世界上所有其他黑客)的时间。

这个项目的软件部分，他称之为 BitsyLED，实际上由两部分组成。首先是固件本身，它旨在控制常见的 RGB LEDs，如 WS2812 或 NeoPixel 系列的成员。它可以在 Arduino Pro Mini 上运行，没有任何问题，但[Andy]也基于 ATtiny84 设计了自己的开放式硬件控制板，您可以自己构建。目前你需要一个 USBASP 来编程，但他正在开发第二个版本，将增加 USB 支持。

当您选择的控制器运行 BitsyLED 固件时，您需要一些东西来配置它。为此，[Andy]开发了一个 Chrome 扩展，为设置颜色和图案提供了一个非常光滑的用户界面。该工具甚至允许您创建 led 的可视化表示，以便您可以了解当所有硬件通电时它会是什么样子。

[ws 2812 等 RGB LEDs 是我们今天在项目中看到的一些最常见的元件](https://hackaday.com/2019/03/26/can-you-live-without-the-ws2812/)，主要是因为它们非常容易与微控制器进行物理接口。但是即使[只需要几根电线来控制大量的发光二极管](https://hackaday.com/2019/03/20/an-esp8266-sundial-for-your-wall/)，你仍然需要为这一切编写代码。BitsyLED 消除了最后一部分的许多麻烦，我们非常有兴趣看看黑客社区是如何看待它的。

 [https://www.youtube.com/embed/e7a4mR2vg3Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/e7a4mR2vg3Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

