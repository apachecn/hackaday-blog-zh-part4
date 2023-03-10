# 谁在门口

> 原文：<https://hackaday.com/2021/07/13/nfc-whos-at-the-door/>

![RevK_NFC_v1-Prototype-Photo](img/1167cec194268691f088ba0437ab359d.png)

An early prototype that worked on the first try, except for one LED

[RevK]想要了解 NFC 读卡器，我们一致认为最好的方法是[自己动手制作一个](https://www.revk.uk/2021/04/well-i-made-one.html)。

有多种来源的阅读器，但[RevK]发现它们要么[紧凑但没有原型空间](https://www.elechouse.com/elechouse/index.php?main_page=product_info&cPath=90_93&products_id=2276)，要么有足够的原型空间和[大的占地面积](https://www.adafruit.com/product/364)。选择高速 UART (HSU)而不是 I2C 与 ESP32 进行通信，因为测试表明，它在长距离上同样快速且更可靠，只需增加一根电线。

几个版本之后，基于 PN532 的 NFC 阅读器的 GPIO 刚好够门铃和防篡改开关以及三个状态 led，电路板文件和 3D 打印外壳设计包含在 GitHub 上的开源项目[中。在研究该项目时，我们感谢](https://github.com/revk/ESP32-PN532)[了解防篡改开关](https://www.youtube.com/watch?v=3uknXCNwjH8)，当读取 NFC 时，它可以包括闭合或断开的接触状态，最常用于高价值和可收藏产品的包装。如果你使用过 NFC 的这个篡改特性，请告诉我们。

谢谢你的提示，[西蒙]