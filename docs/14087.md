# 树莓皮微微 W 添加无线

> 原文：<https://hackaday.com/2022/06/30/raspberry-pi-pico-w-adds-wireless/>

来自 Raspberry Pi 的消息:[他们的 Pico 的最新版本有 WiFi](https://www.raspberrypi.com/news/raspberry-pi-pico-w-your-6-iot-platform/) ，显然被称为 Pico W。我们打算得到一个样本单元，踢它的轮胎，但它在海关卡住了。嘘！因此，在它出现之前，我们可以从新闻稿和文档中收集到以下信息。

当然，Pico 是基于 RP2040 微控制器的 Raspberry Pi 微控制器开发板。这又有两个 Cortex M0+内核和一大块板载 RAM，这使它成为 MicroPython 的热门目标。他们在 PCB 上有一些额外的空间，所以他们增加了一个英飞凌 CYW43439 WiFi 芯片，瞧:Pico W。

截至目前，WiFi 在 [C SDK](https://github.com/raspberrypi/pico-sdk) 和预烘焙的 MicroPython 映像中都得到了支持。让它工作起来看起来非常简单，而且它是基于久经考验的 [lwIP 栈](https://savannah.nongnu.org/projects/lwip/)，嵌入式世界的经典。CYW43439 也具有蓝牙功能，但还没有固件支持，但如果它很快出现，我们不会感到惊讶。

价格？整个射击比赛 6 美元。你可以从两个方面来看待这一点:比老款 Pico 高出 2 美元，或者价格上涨 50%。你如何看待事情可能取决于你的订单数量。无论哪种方式，它都在 ESP32 模块的价格范围内，所以如果您的项目需要微控制器和 WiFi，您可以进行一些比较。在硅短缺的今天，有几个选择是很好的。