# 将蒸汽控制器与 LEGO Motors 一起使用

> 原文：<https://hackaday.com/2020/04/01/using-the-steam-controller-with-lego-motors/>

虽然 Valve 的蒸汽控制器最终是一个商业失败，但不可否认它是一个有趣的硬件。凭借双触控板、丰富的按钮和蓝牙功能，它可能是控制您下一个版本的理想方式。多亏了[geggo]最近的一个项目，[现在你甚至有了一个可以效仿的榜样](http://www.g3gg0.de/wordpress/programming/legoremote/)。

[![](img/13a77ceb0bb4a8cc5acd5e39156350ee.png)](https://hackaday.com/wp-content/uploads/2020/03/steamlego_detail.jpg) 一个装有 ESP32 和 DRV8833 双 H 桥电机控制器的定制 PCB 用于与标准 LEGO 电机接口，这些电机使用它们的积木式连接器。这意味着，无论你已经建造了什么样的机动化产品，这种板都是一种直接升级。

由于 ESP32 显然除了蓝牙之外还有 WiFi，这也意味着这个小电路板可以通过本地网络甚至互联网控制乐高项目，只需对固件进行一些更改。

有趣的是，虽然 Valve 在 2018 年正式启用了蒸汽控制器上的蓝牙，但听起来似乎需要一些未记录的戳和逆向工程才能让它在这里工作。对于我们这些喜欢好的黑客来说，这很好，但是如果你更感兴趣的只是让事情正常运行，[geggo]已经足够好了，可以发布源代码让你开始。

如果你对蓝牙不感兴趣，但想让你的作品动起来，我们最近报道了一名黑客[如何使用 ESP8266 将他的乐高火车](https://hackaday.com/2020/03/22/motorized-lego-train-gets-qi-charging-in-the-track/)集成到他的智能家居中。

 [https://www.youtube.com/embed/-2-QGO-eoNQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/-2-QGO-eoNQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

