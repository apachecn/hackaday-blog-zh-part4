# Pi 计算模块是 Raspberry 和 Arduino 的私生子

> 原文：<https://hackaday.com/2020/12/14/pi-compute-module-is-love-child-of-raspberry-and-arduino/>

Raspberry Pi 计算模块是一个强大的硬件，尤其是在价格方面。有了它，您可以获得比普通 Pi 更多的 IO，并且能够围绕它设计专门为您的需求定制的硬件，而不仅仅是针对通用消费者。然而，这是以需要一种与之接口的方法为代价的，因为计算模块没有正常的 IO 引脚或端口，但[Timon]为这个模块提供了一个方便的开发板，称为 Piunora，它解决了许多原型问题。

开发板将计算模块扩展到熟悉的类似 Arduino 的外形，并配有 IO 接头、USB 端口和 HDMI 输出。然而，这还不止于此。它有一个 M.2 连接器，一些内置 led，一个摄像头连接器和一些其他功能。它还开辟了一些其他的可能性，这些可能性对于标准的 Pi 4 来说是困难的或不可能的，例如将 Pi 作为 USB 小工具而不是主机设备运行的能力，这简化了某些类型的开发，这是[Timon]的预期功能。

作为开发板，与标准的 Raspberry Pi 相比，这个项目在计算模块的特殊用途方面有很大的潜力。对于嵌入式应用程序来说，部署要容易得多，代价是增加了开发成本。如果你仍然不确定如何使用计算模块 4，我们为你准备了一些阅读材料。而丁满的[前作](https://hackaday.com/2020/11/13/easy-carrier-board-for-the-compute-module-4-shows-you-can-do-it-too/)就是一个很棒的跳板。