# 物联网家庭安全监控

> 原文：<https://hackaday.com/2020/01/17/home-safety-monitoring-with-iot/>

家庭自动化是一个受欢迎的项目，但它的复杂性会很快变得令人生畏，特别是如果你不仅仅是控制几个灯(或者如果你是一个租户)。为了试水，你可能想从像这个家庭安全监控器这样的东西[开始，这是一个基于 Arduino 的物联网设备。它允许远程监控家中的温度、有毒气体、光线和其他变量，即使你不需要或不想控制任何东西，这也是有价值的。](https://hackaday.io/project/169289-home-safety-monitor-using-arduino-and-ubidots)

该设备围绕 Arduino Nano 33 IOT 构建，具有 WiFi 和蓝牙功能以及一些集成的安全功能。这个建筑有许多传感器，包括压力/湿度、气体/烟雾探测器和光传感器。为了报告它在家中收集的所有信息，Ubidots 的接口被配置为允许轻松(安全)地访问设备收集的数据。

该项目的 PCB 和代码都在项目页面上提供，如果 Ubidots 不是你与物联网接口的首选方法，还有许多其他选项可用。如果你愿意的话，你甚至可以试试 [Mozilla 的 WebThings](https://hackaday.com/2019/10/29/mozilla-webthings-an-open-platform-for-building-iot-devices/) 。