# Arduino 进入云端

> 原文：<https://hackaday.com/2019/02/07/arduino-enters-the-cloud/>

不管你喜不喜欢，对许多人来说，嵌入式系统意味着 Arduino。现在，Arduino 正在利用其更强大的 MKR 板，并引入云服务[Arduino 物联网云](https://blog.arduino.cc/2019/02/06/announcing-the-arduino-iot-cloud-public-beta/)。目标是让 Arduino 程序从云中记录数据和控制动作变得简单。

这个[程序处于测试阶段](https://create.arduino.cc/iot/)，具有多种人机交互风格。简单来说，你可以组装一个控制面板，让物联网云生成你的代码，并将其下载到你的 Arduino 本身，无需用户编程。更高级的用户可以使用 HTTP REST、MQTT、Javascript、Websockets 或一套命令行工具。

该系统依赖于温度传感器、发光二极管和伺服系统等“东西”。现在所有的注意力都集中在安全性上，所以系统支持双向流量的 X.509 认证和 TLS 安全性也就不足为奇了。

老实说，我们试过了，基于 web 的 IDE 在 Linux 下找不到我们的 MKR1000 板。对我们来说，这可能是一个错误的配置，但令人沮丧的是，你从许多基于网络的工具中获得的信息是如此之少。它决定我们有多个 Arduinos 连接(我们没有)。然后删除一个多端口串行适配器使它看不到 Arduinos，即使有一个 MKR1000 Vidor 连接。

自然，在将设备放到云上时，有很多选择。然而，如果你只使用 Arduino 板，这将是非常无缝的——假设它适合你。