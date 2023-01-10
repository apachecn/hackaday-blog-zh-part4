# 通过 ESP8266 观看人类大战僵尸

> 原文：<https://hackaday.com/2019/02/08/humans-vs-zombies-via-the-esp8266/>

僵尸，在很大程度上，仍然是虚构的，尚未困扰人类社区。尽管我们面临许多现实世界的灾难，僵尸的概念仍然是一个引人注目的概念，也是许多书籍、电影和视频游戏的主题。[CNLohr]在 MagStock Eight 遇到[Aaron]时，他已经开发了一款这种风格的真实世界游戏。 (YouTube，下面嵌入。)

[Aaron]的游戏名为 SpyTag，由一群人玩，每个人手腕上都戴着一个小装置。两个玩家开始是僵尸，其余的是人类。僵尸可以使用他们的设备作为邻近探测器来追捕附近的人类，人类可以使用他们的设备来探测附近的僵尸，帮助他们逃跑和躲避。

这些设备使用 ESP8266 在 AP+站模式下运行。近程传感的工作原理非常简单。设备通过显示为同名的 WiFi AP 来显示其人类或僵尸状态，邻近检测通过在设备上的 LED 条上显示对面 AP 的信号强度来实现。一旦僵尸离人类设备足够近，人类就会被感染，自己也变成僵尸。

这是一个整洁和轻量级的方式来实现游戏，不需要基础设施或支持玩家腕带硬件以外的硬件。虽然这种方法可能容易受到欺骗，[CNLohr]报告说，未来的工作可能会转向使用 ESP-NOW 协议，使游戏更加安全。

[【Aaron】在 Github](https://github.com/adangert/SpyTag-Wifi-game) 上分享了这个项目，供那些对深入研究代码感兴趣的人参考。我们以前见过类似的游戏，[用 IR 代替。](https://hackaday.com/2015/09/25/becoming-a-zombie-with-the-hackable-electronic-badge/)休息后的视频。

【感谢 Baldpower 的提示！]

 [https://www.youtube.com/embed/TjCUs_oYcsY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/TjCUs_oYcsY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

