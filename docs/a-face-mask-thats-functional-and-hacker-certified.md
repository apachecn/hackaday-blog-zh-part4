# 一个功能性和黑客认证的面罩

> 原文：<https://hackaday.com/2020/07/27/a-face-mask-thats-functional-and-hacker-certified/>

[splat238]需要一个在公共场合戴的面具，但他想要一个比其他人戴的布面具更符合他个人风格的东西。因此，他使用令人印象深刻的 104 新像素升级了他的旧气枪网状面罩，创造了他的[新像素 led 面罩](https://www.instructables.com/id/Neopixel-LED-Face-Mask/)。

新像素基于流行的 WS2812b LEDs。这些是可单独寻址的 RGB 发光二极管，发出令人印象深刻的光芒。[splat238]购买了一个 144 新像素条，以避免一个接一个地焊接这些 104 新像素。他将 144 个 LED 条切割成更小的片段，以帮助将 LED 安装在面罩周围。然后，他将电源线和数据线焊接在一起，这样他仍然可以控制 led，就好像它们是一条线，而不是他切割成的几段线。他需要一个相当大的电池组来驱动整个系统。你可以想象 104 个 RGB LEDs 需要多少功率才能运行。我们建议下次添加电池保护电路，因为这些 led 可能会消耗大量电流。

他设计了自己的控制板，采用 ESP8266 微控制器。鉴于其相当大的内部存储器，ESP8266 可以轻松存储各种 LED 模式，而不必担心编程空间不足。他还希望在他的面具的后续版本中增加一些 WiFi 功能，[所以 ESP8266 是一个显而易见的东西](https://hackaday.com/2018/07/27/esp8266-internet-controlled-led-dimmer/)。此外，他的控制板具有三个按钮，允许他在不同的 LED 模式之间切换。

很酷的项目[splat238]！期待 WiFi 版。

 [https://www.youtube.com/embed/gnIS7tqx5eU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/gnIS7tqx5eU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

