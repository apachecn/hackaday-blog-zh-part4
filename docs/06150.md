# DIY ESP32 报警系统利用 433 MHz 传感器

> 原文：<https://hackaday.com/2020/04/02/diy-esp32-alarm-system-leverages-433-mhz-sensors/>

从 PIR 运动探测器到门窗传感器，433 MHz 报警系统硬件有着巨大的市场。如果你想让它们工作，你只需要一个接收器，一个支持网络的微控制器和一些代码。在他的最新视频中， [[Aaron Christophel]展示了这有多简单。](https://github.com/atc1441/DiyArduinoESP232AlarmSystem)

本质上，您将一个常见的 433 MHz 接收器模块连接到一个 ESP32 或 ESP8266 微控制器，并让它等待，直到一个特定的设备发出声音。从那里，ESP 上的代码可以使用任何适合您的目的的 API 来启动。在这种情况下,[Aaron]使用 Telegram API 发送消息，当门或窗被打开时，这些消息会在他的手机上弹出通知。但是您也可以使用 MQTT 之类的东西，或者如果您想使用传统的方法，让它切换一个连接到响亮警报器的继电器。

即使您不打算制作自己的临时警报系统，如果您想开始使用 433 MHz 硬件，休息后的代码和视频也是一个很好的例子。具体来说，[Aaron]引导查看者扫描新的 433 MHz 设备，并将它们的唯一 id 添加到代码将监听的列表中。如果你曾经想知道用这种东西多快可以启动并运行，现在你已经有了答案。

在过去，我们已经看到过[Raspberry Pi 充当这些类型传感器的 RF 到 WiFi 网关](https://hackaday.com/2018/08/29/raspberry-pi-as-433-mhz-to-mqtt-gateway/)，以及[将它们整合成一个廉价的完整家庭自动化系统](https://hackaday.com/2016/05/01/minimal-433-mhz-web-home-automation/)的项目。

 [https://www.youtube.com/embed/t-DzMOte1Eo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/t-DzMOte1Eo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

