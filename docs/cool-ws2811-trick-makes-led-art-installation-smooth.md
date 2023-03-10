# 酷 WS2811 技巧使 LED 艺术安装顺利

> 原文：<https://hackaday.com/2021/07/27/cool-ws2811-trick-makes-led-art-installation-smooth/>

通常，当一个项目需要可寻址 LED 时，我们只需将一个 WS2812s 和一个 Arduino 放在一起，从 FastLED 库中的示例中拼凑一些代码，然后就可以结束了。我们不会过多考虑幕后发生的事情，除非我们遇到更具挑战性的 LED 项目。

发明家[Leo Fernekes]最近发现自己就处于这样的境地，当时他参与了一个 LED 艺术装置。该项目要求在一个私人庄园的树干周围安装 led 灯条环。然而，项目的实际规模和美学要求带来了巨大的挑战。其中之一是找到一种控制 LED 灯条的方法，每个灯条消耗大约 100 毫安，需要非常平滑地变暗。[Leo]查看了 WS2811 LED 驱动器，但发现低驱动电流和 8 位 PWM 输出都不符合要求。

[Leo]通过同时使用芯片上三个 PWM 通道中的两个来解决这两个问题，一个用于控制电流，一个用于 PWM LED。他想出的电路看似简单——只有四个晶体管、一个肖特基二极管和一堆无源元件。另一个巧妙之处是 LED 条之间的数据接口，可以配置为单端或差分。这允许相同的接口用于树上的短距离杆和树上的长距离杆。

像往常一样，[Leo]很好地解释了他的设计以及它是如何工作的，我们发现这很有指导意义。当他设法调暗一个不可调光的 LED 灯具时，他做了类似的事情。

 [https://www.youtube.com/embed/pZl-YRROb4Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/pZl-YRROb4Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

