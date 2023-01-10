# 兼容 HomeKit 的自制 LED 灯条

> 原文：<https://hackaday.com/2022/10/03/homebrew-led-strips-that-are-homekit-compatible/>

谷歌、亚马逊和苹果都在争夺智能家居领域的霸主地位。你可能已经注意到，更便宜的智能灯和类似的东西通常不提供与苹果 HomeKit 系统的连接。然而，如果你想要一些在生态系统中工作的智能照明，而不需要倾家荡产，你可以自己动手打造！

[这个简单的构建](https://www.instructables.com/Homekit-LED-Strip-Using-3-standard-Modules/)使用一个 ESP8266-01S 作为操作的大脑。这是一个精简版，只有两个 GPIO 引脚可用，但对于这项工作来说，这已经足够了。它配有一个简单的继电器，用于开关单色 LED 灯条，以及一个 MP2307 降压转换器用于供电。加载到 ESP8266 上的代码很简单，允许它连接到 Wi-Fi，并与苹果 HomeKit 链接以进行控制。

假设你是一个真正的花里胡哨的人，你想要一个 RGB 可寻址的 led 灯作为你的家庭装备。没问题，你也可以这样做！这很简单，只需将 ESP8266 连接到某个 WS2812B LED 灯带，并刷新模拟 Elgato EVE LED 灯带的正确固件。如果你愿意，你甚至可以在 via the 应用程序上激活特殊的灯光效果，以利用灯带的完全可寻址特性。

这一领域有大量现成的解决方案，但其中许多都非常昂贵，无法满足您的实际需求。有时候建立自己的也更有趣。或者，如果你不喜欢苹果的智能家居解决方案，你可以尝试更开放的替代方案。休息后的视频。

 [https://www.youtube.com/embed/TG9xq7ith0k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/TG9xq7ith0k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

