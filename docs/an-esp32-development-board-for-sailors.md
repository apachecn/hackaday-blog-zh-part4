# 面向水手的 ESP32 开发板

> 原文：<https://hackaday.com/2021/04/25/an-esp32-development-board-for-sailors/>

[Matti Airas]希望有一个更好的电子平台，让他的船更智能、更互联、更安全。他发现传统的船用电子设备价格昂贵，不适合黑客和修补。来自同一供应商的各代设备之间以及不同品牌之间缺乏互操作性也是一个问题。这让他设计了带有 ESP32 的[水手帽——一种海洋专用的开源硬件开发板。](https://hatlabs.github.io/sh-esp32/)

应用包括船只的各种传感器和控制接口，如测量燃油或水位、发动机转速、锚链长度计数器，或设置智能照明或智能制冷控制。该板设计用于传统的 [NMEA 2000](https://en.wikipedia.org/wiki/NMEA_2000) 标准，以及[信号 K](https://signalk.org/overview.html) 。NMEA 2000 被标准化为 IEC 61162-3，但不是开源或免费的。另一方面，Signal K 是[免费和开源的](https://github.com/SignalK)，可以与 NMEA 2000 共存。

海洋环境可能相当恶劣，有极端的温度、雨水、湿度、冷凝和振动。和汽车一样，船只的电气环境也是出了名的嘈杂，[Matti]特别关注噪音和浪涌抑制。该板可以与 12 V 或 24 V 总线系统一起工作，因为板载 DC-DC 转换器的额定输入高达 32 V。电路板与外界之间的连接需要非常坚固，因此它可以根据您的要求接受各种类型的连接器。

水手帽基于一个标准的 ESP32-WROOM-32 模块。接口包括 CAN 总线收发器、光耦合输入和输出、I ² C、1 线和 QWIIC 接口、USB Micro-B 编程连接器，以及几个按钮和 led。所有的 ESP32 GPIO 引脚都端接在一个 GPIO 接头上，跳线选项可以禁用标准接口的端接，而是根据需要将它们路由到 GPIO 接头。此外，还有一个很大的原型制作区域，可以向电路板添加额外的硬件。硬件设计文件存放在 GitHub 的[项目库](https://github.com/hatlabs/SH-ESP32-hardware)中。

软件方面，有几个框架可以使用，推荐选择 PlatformIO、 [SensESP](https://github.com/SignalK/SensESP) 、ESPHome 和 Visual Studio Code。或者您可以使用任何广泛可用的用于 ESP32 平台的 SDK——Espressif SDK、用于 ESP32 的 Arduino Core、MicroPython、NodeMCU 或 Rust。

[Matti]的 [NMEA 2000 USB 网关](https://hatlabs.github.io/sh-esp32/pages/tutorials/nmea2000-gateway/)的例子是一个很好的方法，可以让你掌握使用水手帽构建实际项目所需的硬件装配和软件安装。该板设计用于承受恶劣的电气环境。但是，如果要在海上应用中生存，它的机械安装显然需要更多的关注。水手帽可安装在普通可用的 100x68x50 mm 或更大的塑料防水外壳中，防护等级为 IP65 或更高。隔板连接器和电缆密封套也需要适当的额定值，外壳可能需要 IP68 等级的通风插头，以应对外壳内的环境循环。