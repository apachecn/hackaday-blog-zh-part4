# 支持 WiFi 的微型 ARM MCU，适用于小型项目

> 原文：<https://hackaday.com/2018/10/02/tiny-wifi-enabled-arm-mcu-for-tiny-projects/>

自从支持 WiFi 的 ESP8266 微控制器出现以来，似乎突然每个人都提出了支持 WiFi 的项目。但是 ESP8266 并不是镇上唯一的游戏！读者[PuceBaboon]通知我们 Seeed Studios 发布了一款新产品:被富有想象力地称为 [Air602 WiFi 开发板](https://www.seeedstudio.com/Air602-WiFi-Development-Board-p-3140.html)。

该板的核心是微型 [WinnerMicro W600 MCU](http://www.winnermicro.com/en/html/1/156/158/497.html) ，它集成了一个 32 位 ARM Cortex M3 CPU，以及双 UARTs、I2C、SPI 和 I2S 接口，以及一个实时时钟(RTC)。除了这个硬件加密外，还有七个 I/O 引脚(开发板上有五个),您就拥有了一个非常强大的支持 WiFi 的 MCU，可以使用提供的 SDK，使用常见的 ARM 开发工具(例如 Keil)对其进行编程。

在撰写本文时， [W600 模块](https://www.seeedstudio.com/Air602-WiFi-Module-p-3139.html)可以单独购买，尽管它很小，只有 12 毫米 x 10 毫米，价格仅为 1.90 美元——没有天线——正如【PuceBaboon】的[关于该 MCU](https://esp8266hints.wordpress.com/2018/09/26/yaespk-yet-another-esp-killer/) 和开发板的想法中所述。