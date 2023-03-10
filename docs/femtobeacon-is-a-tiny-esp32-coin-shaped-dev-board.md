# FemtoBeacon 是一个很小的 ESP32 硬币形状的开发板

> 原文：<https://hackaday.com/2019/04/28/femtobeacon-is-a-tiny-esp32-coin-shaped-dev-board/>

这些年来，我们的单板微控制器平台变得越来越小，从十年前相对较大的经典 Arduino 和 Beagleboard 外形到今天邮票大小的 Feather 和 ESP 板。但是它们能有多小呢？利用当前的组件，[Femtoduino]认为他们已经解决了这个问题，提供了[一个基于 ESP32 的带 WiFi 和蓝牙的电路板，以及一个直径只有 9 毫米的圆形占地面积的 5v LDO 稳压器](https://hackaday.io/project/165241-femtobeacon-esp32-coin)。

这种不动产的缺乏带来了一些妥协，其中最明显的可能是缺乏空间来提供 I/O 线。它有 SPI、UART 和几条 I/O 线，除了板载 RGB LED，就这些了。但是 SPI 的用途远远超出了它的线路数量，即使只有这么少的线路，也有很多事情可以做。另一个潜在的妥协来自天线，Molex 表面贴装元件，这是 9 毫米圆形电路板的必然结果。

微控制器平台总有一天会变得小到无法使用，但很明显，这个极限还有一段路要走。我们很想看看其他设计师如何回应这个公告板。