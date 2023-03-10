# 微型廉价 ARM 板获得 WiFi

> 原文：<https://hackaday.com/2019/01/28/tiny-cheap-arm-boards-get-wifi/>

在过去的几年里，我们已经看到了将支持 WIFi 的微型控制器放在一个一两美元的模块上的价值。你家里的那些智能灯泡里可能有一个 ESP8266，你可以用这些芯片中的一个构建一个支持 WiFi 的任何东西，几乎不用花钱。现在有了一个新的模块，它将“一个模块上有一个相当强大的微控制器，可以实现 WiFi”的设计理念推向了它的逻辑结论。这是 Seeed 工作室的 W600 模块。它有 ARM Cortex-M3，有 FCC 和 CE 认证，有 WiFi，而且很便宜。这是人们想要的，所以必须有人给他们。

该产品似乎是 Seeed 去年年底发布的 Air602 WiFi 开发板的后续和/或改进。虽然模块本身增加了几个城堡形引脚和一个 RF 罐，但其他规格看起来是一样的。与该模块明显与之竞争的 ESP-8266 相比，Air600 能够通过五个 GPIO 引脚实现 PWM、相当数量的闪存和您想要的所有 WiFi 支持来完成自己的任务。

W600 是整个电路板家族的一部分，模块本身随时可用，但也有几个分线板添加电源和串行连接，[一个更大的分线板](https://github.com/linux-downey/w600_development_board_document)正在努力忘记 Arduino Uno 的引脚错位，因为这是 Seeed，一个通过 Grove 连接器连接一切的电路板。[什么是格罗夫连接器？](https://www.seeedstudio.com/grove.html)它是电源、接地、I2C 或串行接口，我上次检查时没有买到。

W600 及其主板系列将很快发货——毕竟，中国即将关闭两周——并且有计划支持 Arduino IDE、Micropython 和您选择的工具链的 SDK。

ESP8266 还是放 WiFi 的不二之选吗？大概吧。但是这里有更多的竞争。