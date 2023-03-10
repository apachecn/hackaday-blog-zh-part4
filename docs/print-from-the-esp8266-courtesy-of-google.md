# 打印自 ESP8266，由 Google 提供

> 原文：<https://hackaday.com/2019/11/21/print-from-the-esp8266-courtesy-of-google/>

ESP8266 已经成为黑客的首选微控制器，因为它非常容易将芯片连接到网络并与其他设备通信。事实上，它也是荒谬的便宜只是一个意外收获。由于你今天购买的几乎每一件电子产品都足够“智能”，包括某种形式的互联网控制，这意味着这些 MCU 可能会戳戳戳的小工具并不短缺。

[![](img/98595d6a94dff32a336914c791c9fc9f.png)](https://hackaday.com/wp-content/uploads/2019/11/cloudprint_logo.png) 在他们的最新提示中，【TecnoProfesor】展示了如何[将 ESP8266 与谷歌的云打印](https://www.instructables.com/id/Printing-From-ESP8266-NodeMCU/)对接，这是一种可以通过网络实现简单远程打印的服务，而不必担心是否有合适的设备驱动程序。从 ESP8266 进行远程打印乍一看似乎只是一个笑话，但是如果你是那种喜欢数据硬拷贝的人，那么为你的气象站添加生成每日打印报告的功能可能是一个不错的周末项目。

[TecnoProfesor]提供了从 ESP8266 的内部闪存和 SPI 附加 SD 卡打印各种尺寸文档的说明和源代码。在这篇文章的最后，甚至有一些关于如何在更高级的场景中使用云打印 API 的`setPrintDocument()`功能的解释，比如打印网页或存储在 Google Drive 中的文档。

当我们看到连接到打印机的微控制器时，[它们通常是小型热敏型的](https://hackaday.com/2010/08/30/arduino-based-thermal-printer/)。能够用如此简单的技术访问“真正的”打印机提供了一些有趣的可能性，尽管像大多数技术一样，[它有被误用的可能性](https://hackaday.com/2018/12/07/weaponized-networked-printing-is-now-a-thing/)。

感谢安德鲁的提示。]