# 一块 ESP8266，一块电池，一年…还在继续。

> 原文：<https://hackaday.com/2020/01/15/one-esp8266-one-battery-one-year-and-counting/>

有时，传感器需要在长时间内不需要人工关注的情况下完成工作，对于这些应用，极低的功耗是必不可少的。[Dave Davenport]有一个基于 EPS8266 的湿度传感器，对每隔几个月就必须更换 AA 电池感到失望。凭借 18650 锂离子电池和一系列节能技巧，时间已经延长到一年多，并且仍在继续，所以[他写了一篇博客，详细介绍了他是如何做到的](https://blog.sarine.nl/2020/01/01/1-year-sensor.html)。

他的一些技巧很简单，比如关闭传感器，或者使用比 Wemos 更好的 LDO 调节器。但其他一些是意想不到的，例如在睡眠期间使用与板载 RTC 相关的内存来存储 WiFi 连接信息和频道号。正常的 ESP8266 连接序列涉及网络扫描，通过保持上次发现的内容，可以避免额外的时间和由此消耗的功率。类似地，从 DHCP 租约切换到固定 IP 地址减少了设备等待租约的时间，从而减少了它必须保持清醒的时间。

我们可能并不都需要构建 ESP8266 湿度传感器，但我们中的许多人都在寻求在项目中降低功耗。让我们帮助你进入竞技场。

ESP8266 图片:Connor good wolf[[CC BY-SA 4.0](https://commons.wikimedia.org/wiki/File:ESP8266_mounted_on_adapter.jpg)。