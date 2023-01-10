# 为智能手机和连接设备添加 LoRa 远程无线电

> 原文：<https://hackaday.com/2019/07/11/adding-lora-long-range-radio-to-smartphones-and-connected-devices/>

你会给你的智能手机增加一个收音机吗？不，不是另一个 WiFi 或蜂窝无线电；智能手机已经具备了这一点。我说的是通过 ISM 频段(433 或 915 MHz)提供连接的东西。这可以在没有手机覆盖的地方使用，而且比 WiFi 覆盖范围更广。这是 Skrypt 背后的想法，一个允许你发送脱离网格消息的消息系统。

Skrypt 是一种基于 ESP32 的硬件调制解调器，可以通过蓝牙或 USB 与智能手机或任何其他设备进行通信。在内部，有两个模块，一个 ESP32 WROOM 模块，提供蓝牙，WiFi，USB 连接，以及所有重要的软件配置和基于 web 的 GUI。LoRa 模块是无处不在的 [RFM95W](https://www.hoperf.com/modules/lora/RFM95.html) ,随时可以放入任何电路。除此之外，整个电路只是一个电池和一些电源管理 IC。

虽然 LoRa 肯定不是你用来将图片转发到 Instagram 的协议，但对于长距离传输的短信来说，它是一个非凡的协议。当你不在手机信号塔的覆盖范围内时，这正是你想要的——这些照片可以等一等，但你可能真的想给你的朋友发几个字。这是非常宝贵的，劳拉在这种情况下很有意义。

The [HackadayPrize2019](https://prize.supplyframe.com) is Sponsored by: [![Supplyframe](img/79a7db035b8a2b6c2b7b0895c45b7de8.png)](https://supplyframe.com/)  [![Digi-Key](img/ba094a14c430ab81591a2abdc54a5363.png)](https://hackaday.io/digikey)  [![Microchip](img/5023ef0b7ff1aee311cba9b54a3ac9fe.png)](https://hackaday.io/microchip)