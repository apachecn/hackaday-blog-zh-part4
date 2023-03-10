# 用 WebUSB 入侵 Arduino NFC 读卡器

> 原文：<https://hackaday.com/2020/01/01/hacking-an-arduino-nfc-reader-with-webusb/>

当[g archen]想要读取一些 NFC 标签时，他经历了几次迭代。首先，他尝试了一个电子应用程序，然后是客户端-服务器架构。但他的最后一次迭代是让[成为一个带有 Arduino 的独立阅读器，并使用 WebUSB](https://github.com/gdarchen/webusb-arduino-nfc/tree/master/3-webusb) 连接到 PC 上的应用程序。

这听起来很容易，但要做到这一点需要一些技巧。他必须黑掉电路板才能正确连接 NFC 阅读器的中断，因为他使用的是莱昂纳多电路板。但是最大的问题是启用 WebUSB 支持。有一个库，但你必须转换你的 Arduino 才能使用 USB 2.1。事实证明，这并不难，但有一个警告:一旦你做了这种改变，你将需要在你的所有程序 WebUSB 库或 Windows 将拒绝识别 Arduino，你将无法轻松地重新编程。

一旦你解决了这些问题，剩下的就很容易了。PC 端使用 node.js，如果在 GitHub 库中备份一个关卡，也可以看到早期的非 Arduino 版本的代码。

如果你想了解设计中的所有逻辑，作者还提供了一个讨论三个版本及其优缺点的幻灯片。他确实提到他想要一个短程解决方案，所以条形码和二维码被淘汰了。他也决定反对 RFID，但没有真正说出原因。

[NFC 名片](https://hackaday.com/2017/10/25/nfc-enabled-business-card/)是个东西。你也可以用它们来搭乘一些[公共交通](https://hackaday.com/2017/06/20/making-a-wearable-nfc-bus-pass/)。