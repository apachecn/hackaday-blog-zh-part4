# ESP32 专用 LED 动画框架

> 原文：<https://hackaday.com/2021/08/02/dedicated-led-animation-framework-for-esp32/>

[Eric Arcana]几年来一直在创作动画节日装饰品，其中涉及大量定制代码，以他想要的方式照亮事物，拉动微控制器进行更改。使用带有远程软件更新的 ESP32s 更容易，但[Eric]也想使代码更简单。为了实现这一点，他创建了 [Fade](http://www.riderx.info/fade-an-esp32-animation-system/) ，这是一种定制的编程语言/框架，用于控制来自 ESP32 的 LED 动画。

Fade 专为 Neopixel/WS2812 等可寻址 RGB LEDs 而设计。它跟踪系统中每个 LED 的当前颜色，并允许用户定义未来某个特定时间的颜色。时间用 10 ms 时钟周期指定。led 将在指定数量的时钟周期内从一种颜色平滑地变为另一种颜色，而不需要指定中间颜色应该是什么。

代码用简单的 IDE 编写，运行在 ESP32 本身的 web 服务器上，或者运行在远程 Windows PC 上。该语言非常简单，但仍然强大到足以创建复杂的 LED 动画。它的一个关键部分是能够在几行代码中指定多个并发的状态变化。[Eric]还包括选择触摸按钮输入，并使用它们来更新动画。另一个不错的特性是桌面 IDE 上的模拟窗口。它允许您在 PC 上创建自定义 LED 布局，并测试您的代码，而无需将其发送到 ESP32。

可寻址 LED 使得大型 LED 安装变得更加简单，比如这个 [6 英尺的 LED 球](https://hackaday.com/2012/09/11/disco-planet-a-massive-rgbw-led-array-in-a-6-globe/)或者一个 [LED 视频墙](https://hackaday.com/2019/05/17/a-ping-pong-ball-led-video-wall/)。

 [https://www.youtube.com/embed/-CXQz1x2k9o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/-CXQz1x2k9o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

