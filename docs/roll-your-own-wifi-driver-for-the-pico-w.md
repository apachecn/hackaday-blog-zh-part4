# 为 Pico W 开发您自己的 WiFi 驱动程序

> 原文：<https://hackaday.com/2022/12/13/roll-your-own-wifi-driver-for-the-pico-w/>

Raspberry Pi Pico 是一个方便的小型微控制器，已经成为许多黑客工作台的广泛补充。Pico W 有一个 CYW4342W 模块(就像 Pi Zero W 一样)来添加 WiFi 功能，【杰里米·边沁】[将其裸机 WiFi 驱动程序移植到 Pico W](https://iosoft.blog/2022/12/06/picowi/) 。

CYW43438 是一个 SDIO 接口，所以大部分代码都是从他的 Zerowi 项目移植过来的，但在这个过程中也有一些值得注意的调整。鉴于 Pi Pico SDK 拥有驱动 CYW43439 和开源 TCP/IP 堆栈(lwIP)的完整源代码，并且英飞凌的数据表非常详细，为什么要创建自己的驱动程序呢？

简短的回答是…因为为什么不。但是第二个答案是按照你喜欢的方式来调整它。通过他自己的实现，[Jeremy]可以专注于最大化吞吐量，并使 WiFi 更容易调试。他深入研究了硬件、范围跟踪和代码示例。这是一篇在午餐时阅读的精彩的五集读物。一些亮点包括为 PIO(可编程 I/O)编写一些代码以与 SPI 接口接口，WiFi RAM 中的存储体切换，处理 140 个不同的事件，连接到网络，以及发送 pings。

PicoWi [代码可以在 GitHub](https://github.com/jbentham/picowi) 上获得。也许它可以[与这个 PCMIA 接口](https://hackaday.com/2022/09/25/pi-pico-w-does-pcmcia-gets-this-ibm-pc110-online/)集成在一起，为一台旧笔记本电脑提供出色的性能。