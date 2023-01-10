# 具有新分组无线电的双向 IP

> 原文：<https://hackaday.com/2019/03/30/bidirectional-ip-with-new-packet-radio/>

如果你想在业余无线电上联网计算机，有几个选择。有各种各样的 WiFi 黑客，当然还有分组无线电。[新的分组无线电](https://hackaday.io/project/164092-npr-new-packet-radio)，一个来自[f4hdk]的项目，现在在 hackaday.io 上，与我们以前见过的任何东西都不一样。这是一个现成的调制解调器，使用标准的 433 ISM 频段芯片，建造成本应该只有 80 美元，而且它支持双向 IP 流量。

这个项目的介绍性文档 (PDF)展示了 NPR 的用例、协议和硬件。它基于专为 433MHz ISM 频段设计的芯片，特别是来自 Silicon Labs 的 SI4463 ISM 频段无线电。使用现成的放大器，调制解调器的其余部分由 Mbed Nucleo 和 Wiznet W5500 以太网模块组成。主设备和客户端只有一种调制解调器类型。该网络被设计成一个主服务器作为 [Hamnet](http://www.philsherrod.com/hamradio/Hamnet.pdf) 之间的桥梁，这是一个高速网状网络，可以连接到更广泛的互联网。该主机最多可同时连接七个客户端。或者，有一种点对点配置，允许两个客户端以大约 200 kbps 的速度相互连接。

作为一个 434 MHz 的设备，这只是不打算在美国飞，但相关的芯片将与 915 MHz ISM 波段。这是 IP over radio 的一个很好的解决方案，像许多流行的业余无线电项目一样，它首先从硬件黑客开始。