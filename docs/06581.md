# 天气显示多云，有 8266 的可能性

> 原文：<https://hackaday.com/2020/05/19/weather-display-is-cloudy-with-a-chance-of-esp8266/>

[Mukesh Sankhla]写来分享这个独特的天气展示，它看起来是艺术和科学的平等部分。这款设备通过嵌入 3D 打印结构的 25 个 WS2812B LEDs 向用户传达各种天气情况，而不是用数字等平淡无奇的东西来显示当前的情况。它还可以兼作办公桌的实用花盆。

那么这种盆栽植物是如何告诉你是时候拿伞了呢？使用 NodeMCU ESP8266 开发板，它连接到 openweathermap.org，并获得您所在位置的当前条件。相对温度是通过改变锅本身的颜色来传达的；随着温度的升高由蓝色变成红色。如果下雨，植物上的云会改变颜色并闪烁，以表示打雷。

[Mukesh]提供了印刷组件的所有 STL 文件，以及 ESP8266 的源代码。尽管你需要提供自己的土壤和植物，但你只能通过互联网发送这么多。顺便说一句，如果他在视频中将这些 WS2812B 模块焊接在一起的巧妙方式吸引了你的眼球，[你会非常喜欢我们之前报道的他的“RGB 护目镜”项目](https://hackaday.com/2020/05/08/these-led-shades-will-blind-you-with-science/)。

 [https://www.youtube.com/embed/SQTzGKAYG94?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/SQTzGKAYG94?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

