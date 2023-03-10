# 迫使亚马逊 Alexa 兼容的东西与谷歌助手说话

> 原文：<https://hackaday.com/2019/01/01/forcing-amazon-alexa-compatible-stuff-to-speak-to-google-assistant/>

这花了很长时间，但现在已经是 2019 年了，我们开始习惯与计算机对话的概念，让它控制房子周围的事情。这并不像我们以前在电影中看到的那样酷，但这就是现实生活。问题是，有许多不同的系统和标准，它们不一定能一起工作。在[布莱克]的例子中，问题是伍兹品牌的硬件只能与亚马逊 Alexa 兼容，这根本不行。

[Blake]经历了一系列麻烦，比如让亚马逊 Alexa 兼容 WiFi 插座与谷歌助手配合使用。这是一种有点迂回的做事方式，但它是有效的。使用了 TP-Link HS-105 WiFi 插头，可以通过 Google Assistant 语音命令进行控制。该器件由两块 PCB 组成——一块支持 WiFi 的控制板和一块带继电器的开关板。[Blake]用控制板把它接到树莓派上。当通过谷歌的命令打开时，HS-105 将引脚设置为高电平，这被树莓 Pi 检测到。树莓 Pi 然后运行[一个由伍兹硬件使用的 KAB 协议](https://github.com/blakewford/kab)的软件实现，当它从 TP-Link 硬件接收到信号时触发它。

如果我们理解正确的话，[布莱克]不得不去这个麻烦，以便使他的特殊户外额定插座与他的谷歌主页设置工作。希望互操作性在未来几年得到改善，但我们不会屏息以待。

我们以前在这个领域见过一些非常复杂的项目，经常使用 IFTTT — [像这个 ESP8266 声控坦克](https://hackaday.com/2018/09/06/esp8266-powered-tank-with-voice-control/)。