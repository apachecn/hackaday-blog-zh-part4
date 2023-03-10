# 用 ESP 闪烁 TI 芯片

> 原文：<https://hackaday.com/2022/04/03/flashing-ti-chips-with-an-esp/>

德州仪器因制造过时的计算器并以高价卖给学生而广为人知，但他们也制造一些有趣的(价格合理的)微控制器。虽然不像 Atmel 和 Arduino 平台那样无处不在，但它们仍然可以在许多消费电子产品中找到并被重新编程，并且[Aaron] aka [atc1441] [演示了如何使用 ESP32 作为中介来修改它们](https://github.com/atc1441/ESP_CC_Flasher)。

具体来说，这个版本中的 TI 芯片围绕 8051 核微控制器，这是[Aaron]在小型电子纸价格标签和其他 RF 硬件中发现的。他正在使用 ESP32 对 TI 芯片进行重新编程，并利用 ESP 上的网络服务器，以便能够通过 WiFi 重新刷新它们。一些电子纸显示器具有内置的头部引脚，这使得将它们连接到 ESP 相当容易，一旦解决了这个问题，[Aaron]还提供了一个完整的软件库，用于通过浏览器界面与这些微控制器进行交互。

目前，该项目支持 CC2430、CC2510 和 CC1110 变体，但[Aaron]计划在未来增加对更多变体的支持。这是一个相当全面的构建，比购买专有的 TI 编程器好得多，所以如果你有一些这样的电子纸显示器，进入的门槛已经大大降低了。如果你没有这种特定类型的显示器，我们过去也看到过类似的其他电子纸设备的拆卸和重新利用。

 [https://www.youtube.com/embed/1mIrL0A4vOM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/1mIrL0A4vOM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

