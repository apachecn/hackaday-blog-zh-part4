# APPLE2IDIOT 扩展卡可以让你的 Apple II(有点)接入互联网

> 原文：<https://hackaday.com/2022/05/07/apple2idiot-expansion-card-lets-your-apple-ii-sort-of-access-the-internet/>

[Nathanial Hendler]为 Apple II 系列电脑设计的 Apple2Idiot 扩展卡是现代和古典的巧妙结合，提供了一种聪明的方式，允许主机通过 WiFi(间接)访问互联网，同时从主机的角度保持简单。

[![](img/26529b6389421b5796b1a05085c21e77.png)](https://hackaday.com/wp-content/uploads/2022/05/APPLE2IDIOT-card.jpg)

The PCB has plenty of space on which to silkscreen reference data. Click to enlarge.

它通过在扩展卡上嵌入 ESP32 模块和双端口 RAM 芯片来实现这一点。当安装到主机中时，Apple2Idiot 呈现为主机可以访问的存储器位置。然后，ESP32 负责所有需要互联网接入的 WiFi 通信和任务，主机通过`PEEK`和`POKE`命令指导这些任务(并读取它们的输出)。

这意味着任何给定的任务都有两个软件:一个运行在 ESP32 上执行实际工作，另一个运行在 Apple II 上，通过读写内存与卡上的 ESP32 进行通信。这是一个简单的系统，而且[Nathanial]认为这个系统非常适合特定的任务。

示例程序包括扫描和选择 WiFi 网络、获取天气数据以及向 Slack 发送消息等。开发新的应用程序确实意味着必须在两端编写软件，但系统的简单性也意味着灵活性，因为 ESP32 所做的任何事情都可以在数据呈现给主机时将其复杂性抽象化。这并不是说 Apple II 不能更直接地应对现代互联网；我们已经看到了用 basic 语言编写的基本的 Apple II 网络服务器。