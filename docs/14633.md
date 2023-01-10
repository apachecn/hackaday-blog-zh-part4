# 为您的下一个 RP2040 项目提供一个优雅的以太网库

> 原文：<https://hackaday.com/2022/08/27/an-elegant-ethernet-library-for-your-next-rp2040-project/>

几天前，我们报道了一个项目，该项目使用一些双绞线和一个 RJ-45 连接器将以太网连接到 Raspberry Pi Pico。这是一个巧妙的技巧，但还没有准备好被广泛采用。为了改进一些东西，[tvlad1234]已经将该项目的代码重新编写成一个友好的库，您可以在任何 RP2040 板上使用。

如果你错过了，最初的演示通过与 PIO 进行比特碰撞来进行 [10BASE-T 传输，并且能够向有线局域网上的设备发送 UDP 消息。这是一个令人印象深刻的成就，但它的代码并不容易围绕它构建您的项目。这个新的库使 UDP 消息传递像`printf`一样简单，将所有非 PIO 管理的以太网信号工作卸载到 RP2040 的第二个 CPU 核心上。该库甚至会从你的闪存芯片序列号中生成一个随机的 MAC 地址！](https://hackaday.com/2022/08/26/bit-banged-ethernet-on-the-raspberry-pi-pico/)

作为新库的演示，[tvlad1234]通过 I2C 使用 BMP085 或 BMP180 传感器连接组装了一个简单的[以太网连接温度监控器](https://github.com/tvlad1234/Pico-10BASE-Thermometer/)。如果你觉得你可以在生活中使用以太网传输传感器，浏览源代码将是一个很好的开始。