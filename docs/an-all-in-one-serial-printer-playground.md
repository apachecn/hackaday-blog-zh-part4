# 多功能一体串行打印机游乐场

> 原文：<https://hackaday.com/2022/09/22/an-all-in-one-serial-printer-playground/>

20 世纪 80 年代痴迷于微型计算机的年轻人最渴望的外设之一是打印机，可能是点阵设备。自那以后的几十年里，打印机几乎变成了一件可以丢弃的垃圾，因为廉价的喷墨打印机可以在任何车库销售中找到。不过，这并不是说破解老式打印机就没有太多乐趣，而且还有很多小型热敏打印机可以玩。anmoydutta 提供了一个可能有所帮助的平台，其形式是基于 ESP32 的 C3 串行打印机控制器 T2。

板上有一个电平转换器，用于 5 伏打印机电子设备和所有合适的打印机连接器，以及 ESP 和板载 USB 接口。这是一个联网的打印服务器，但完全可以被黑客攻击。我们认为有问题的打印机是 Adafruit 出售的这台打印机。

因此，这个板使一大堆与打印机相关的项目变得更容易，如果你尝试一下，你无疑会发现自己深陷在小卷纸中。不过，这并不是镇上唯一的打印机，[别忘了便宜的蓝牙打印机](https://hackaday.com/2021/09/21/mini-wireless-thermal-printers-get-arduino-library-and-macos-app/)！