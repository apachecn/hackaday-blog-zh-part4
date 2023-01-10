# 新的 AVR-IOT 板连接到谷歌

> 原文：<https://hackaday.com/2018/10/27/new-avr-iot-board-connects-to-google/>

Hackaday 的读者对使用微控制器将数据推送到 WiFi 并不陌生。即使在 ESP8266 之前，也有多种方法可以做到这一点。现在，Microchip 也加入了这场竞争，它推出了一款售价 29 美元、名为 AVR-IOT WG 的主板，内含一个 8 位 ATmega4808、一个 WiFi 控制器和一个用于谷歌云认证的硬件加密芯片。

该板有一个带 USB 端口的部分，用于给电池充电和调试，看起来像是被切割掉的。有许多发光二极管和按钮，以及一个光传感器和一个温度传感器。感觉这里的目标是将尽可能多的微芯片部件封装到一个开发板上。您会发现 ATmega4808 是主控制器，一个 ATWINC1510 WiFi 控制器(一个让人想起 ESP8266 的齿形模块)，一个 ATECC608A 加密协处理器，MCP73871 LiPo 充电器，MIC33050 稳压器和一个 MCP9808 温度传感器。我们找不到太多关于“nEDBG 编程器/调试器”芯片的信息。如果您已经在少数其他开发板上使用过它，请在评论中告诉我们关于板外编程和其他可能的攻击。

自然，该板与 AVR Studio 或 MPLAB X IDE(微芯片购买了 Atmel，还记得吗？).当然，Atmel START 或 MPLAB 代码配置器也可以配置设备。还有一个 AVR-IoT 品牌的网站,可以让你使用谷歌云连接你的设备进行开发。沿顶部和底部边缘的标题与 MicroElektronika Click boards 兼容，这将使任何拥有满满一箱零件的人感到高兴。

看来你现在可以从平常的地方拿微芯片板了。通过阅读 Microchip 的内容，他们希望将其定位为“物联网 Arduino”——一些没有太多经验的人可以使用它来将数据传输到谷歌云。虽然这可能很好，但使用 Arduino IDE 使用 ESP 设备做同样的事情并不困难，然后你有一个 32 位处理器，你可以使用任何你想要的云供应商。当然，这将是一个多一点的工作，所以也许这就是这个产品的吸引力。

从好的方面来说，我们真的很喜欢有一个电池选项，上面已经有一个充电器——似乎这是我们总是必须添加的东西。它可能被隐藏在文档中，但用户指南和技术指南似乎没有指定平均和最大电流消耗，所以电池寿命是一个开放的问题，尽管视频中说“低功耗”。

虽然这不是完全相同的事情，但我们已经看到了 [ESP8266 与谷歌服务器](https://hackaday.com/2017/05/23/google-home-meets-esp8266/)的对话，用于与谷歌 Home 接口。当它在亚马逊云上时，我们甚至在那里看到了[a 6502](https://hackaday.com/2017/07/08/6502-retrocomputing-goes-to-the-cloud/)。

 [https://www.youtube.com/embed/BqjFZjdBLH8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/BqjFZjdBLH8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

