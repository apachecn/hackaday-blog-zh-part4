# 远程 MQTT 温度传感器展示了它是如何做到的

> 原文：<https://hackaday.com/2022/03/13/remote-mqtt-temperature-sensor-shows-how-its-done/>

首先，肯定有更简单的方法来监控远程温度，但[Mike]的[远程 MQTT 温度传感器和显示器](http://www.whatimade.today/make-a-remote-temp-sensor-with-permanent-display-inside-your-house/)项目在几个方面是有用的。它不仅展示了如何从头开始构建这样一个系统，还展示了太阳能等系统特性。

毕竟，如果一个人只是想监控温度，这很容易做到，但一旦一个人希望记录这些温度并使用它们来触发其他事情，那么推出自己的解决方案就开始变得更有吸引力。这就是使用别人的项目作为设计参考可以派上用场的地方。

[Mike 的]解决方案使用两块 Wemos D1 板:一块带有 DS18B20 温度传感器，用于室外；另一块带有小有机发光二极管屏幕，用于室内显示。外部传感器依靠一个可充电的 18650 电池和一个太阳能电池板来轻松供电，内部传感器(可以有很多)有一个可爱的外壳，由 USB 供电。在后端，运行 MQTT 网关和 Node Red 的 Raspberry Pi 负责操作方面的事情。整个系统已经愉快地运行了两年多。

[什么是 MQTT](https://mqtt.org/) ？它本质上是一个消息协议，负责在物联网设备之间可靠地来回传输数据的整个业务。它的伸缩性很好，不需要很硬或者很吓人；[我们自己的【埃利奥特·威廉姆斯】可以告诉你关于实施它的一切](https://hackaday.com/2016/05/09/minimal-mqtt-building-a-broker/)。