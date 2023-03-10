# 将 ESP-32 连接至以太网

> 原文：<https://hackaday.com/2018/08/19/wiring-the-esp-32-to-ethernet/>

自多年前问世以来，ESP-8266 已经风靡全球。它是数千个不同项目中的芯片，也是数十种不同物联网事物的基础。8266 的后续，ESP-32，能力更强。它内部有大量外围设备，包括一台以太网 MAC。那是什么？是的，可以在 ESP-32 上安装以太网，并为物联网板提供 PoE。这就是[【Patrick】正在为他的 Hackaday Prize 项目](https://hackaday.io/project/85389-wesp32-wired-esp32-with-ethernet-and-poe)所做的，这是一个很棒的想法。

正如您所料，这一构建始于一个 ESP-32 模块连接到电路板的一侧，电路板上有一些 GPIOs 分线点和一个 USB 转串行芯片。这里棘手的部分是以太网的 PoE 部分，它需要 MagJack 以太网连接器、回扫变压器和 PoE-PD 控制器。这些都是昂贵的器件，这种电路板的设计需要一些思考——变压器两端需要隔离，这种情况下需要适当的接地层。

在有线配置中使用 ESP-32 有些小聪明。我们经常看到这些模块被用作传感器网络中的无线节点。电池消耗很大，所有这些制造商都在他们花哨的 WiFi 传感器网络中添加 USB 电源输入。如果你无论如何都要用电线供电，为什么不添加以太网，摆脱所有的无线设置呢？这是一个伟大的项目，也是今年 Hackaday 奖的最佳作品之一。

The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)