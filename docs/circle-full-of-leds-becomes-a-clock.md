# 布满发光二极管的圆圈变成了一个时钟

> 原文：<https://hackaday.com/2021/02/27/circle-full-of-leds-becomes-a-clock/>

对于黑客来说，建造某种类型的时钟似乎是一个由来已久的传统，而 LED 时钟似乎是最受欢迎的一种。你可以建造任何东西，从七段显示器到二进制时钟，甚至更奇特的东西。【独领风骚】在网上找到了一圈 LED 环，并制作了一个 [LED 版本的模拟时钟](https://github.com/MilovdZee/LEDCircleClock)。

[![](img/46f3a8b342b281e48ad555cd980d5000.png)](https://hackaday.com/wp-content/uploads/2021/02/241LEDring.jpg)

这些环没有连接在一起，看起来它们是分开设计的，但很容易将它们连接在一起，以形成一圈单独可访问的 RGB LEDs。时钟的每个指针都是不同的颜色，并且经过抗锯齿处理，看起来更加平滑，因为 led 没有排成一行。[Clueless]想要秒针平稳地旋转，所以它使用毫秒作为秒针的偏移来更新。ESP8266 运行代码并控制 led 从 NTP 服务器获取时间。偶尔，[独领风骚]会让时钟显示一个快速效果，比如吃豆人或者雷达扫描动画。

所有的文件都在 Github 页面上[，包括案件的搅拌机模型，可以用来制作你自己的，简单地搜索“241 LED 环”就可以找到所用的 LED 硬件。网站上有很多时钟项目，像这个](https://github.com/MilovdZee/LEDCircleClock)[多色 LED 环钟](https://hackaday.com/2018/04/01/multi-coloured-leds-make-for-a-beautiful-colour-clock/)，我们相信你可以找到[一些](https://hackaday.com/2020/04/15/led-clock-strips-time-down-to-pulses-of-light/) [有趣的](https://hackaday.com/2017/10/02/7-segment-digits-slide-stylishly-on-this-oled-clock/)。

 <https://hackaday.com/wp-content/uploads/2021/02/LayoutVideo.mp4?_=1>

[https://hackaday.com/wp-content/uploads/2021/02/LayoutVideo.mp4](https://hackaday.com/wp-content/uploads/2021/02/LayoutVideo.mp4)