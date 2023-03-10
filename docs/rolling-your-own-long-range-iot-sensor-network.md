# 打造自己的远程物联网传感器网络

> 原文：<https://hackaday.com/2021/11/11/rolling-your-own-long-range-iot-sensor-network/>

自制无线传感器在这些地方并不新鲜:拿起一个 ESP8266，把一个 BME280 挂在 I2C 的针脚上，你只需要几行代码就可以按照自己的方式加入物联网。像这样的构建是如此便宜和容易，以至于它们对于那些希望进入电子游戏的人来说是一个很好的第一个项目，但是如果你正在寻找一些更定制的东西呢？

在这种情况下，你可以跟随[【谨慎的市长】的脚步，为远程无线传感器](https://hackaday.io/project/182274-long-range-iot-everywhere)组装一个定制的模块化架构。该系统的核心是德州仪器 SimpleLink CC1312 无线 MCU 的分线板，它具有一个简单的 2×11 接头连接器。这使得模块既可以插入更大的电路板，也可以直接连接一个小的传感器 PCB。

[![](img/9cafc6d9e7b17239637ad003f5ece441.png)](https://hackaday.com/wp-content/uploads/2021/11/cc1312iot_detail2.jpg) 这些主板不使用 WiFi，也不需要一些现有的无线电基础设施，而是使用 IEEE 802.15.4 标准在高达 600 米的范围内自动创建一个专用网络。不需要专门的接收器，从网络上获取数据，一个 CC1312 板只需通过一个简单的 FT232 适配器连接到计算机。

[Discreet Mayor]已经创造了许多使用这些定制无线电进行通信的项目，从泳池监控系统到烧烤用的[温度传感器](https://hackaday.io/project/182323-long-range-thermocouple-temp-sensor)。便携式电池供电设备能够像市电供电的静态设备一样使用这种常见的通信主干，这是对固件尽可能稳定高效的努力的证明。

喜欢远程专用网络的想法，但不太热衷于必须拿出自己的硬件？别担心。整个夏天，Espressif 宣布他们正在开发一个包含 IEEE 802.15.4 支持的 ESP32 变体[。一旦芯片短缺结束，我们甚至可以看到这个东西。](https://hackaday.com/2021/08/04/new-part-day-an-esp-with-zigbee/)