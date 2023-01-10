# 告诉你天气的伞

> 原文：<https://hackaday.com/2018/12/25/the-umbrella-that-tells-you-the-weather/>

大多数人可以告诉你伞的各种用途——它可以挡雨，戳醒熟睡的火车乘客，还可以在热狗线上的紧张局势达到沸点时用作临时防御武器。当然，一个真正的英国人绝不会如此轻率地使用他们的马车，但他们可能会通过打包一个完整的气象站来升级马车。

![](img/722562e4a91a91df09f4190c5b6c1dbb.png)

Please do not message us to complain about the redundancy of a rain sensor on an umbrella.

建造使用粒子光子作为操作的大脑，将它与几个传感器连接起来。有一个 DHT11 来处理温度和湿度测量，一个 Adafruit 气压传感器，以及一个定制的风速计，使用带 3D 打印风杯的有刷电机。最后，基于与汽车应用相同的原理，试验板变成了雨水检测器。

粒子光子使用 WiFi 连接到智能手机，通过 Adafruit IO 将收集的数据传输到云端。这使得数据能够在个人电脑上进行整理和进一步处理。是的，现在是 2018 年，他们现在在雨伞上有互联网。

随着我们进入更深的冬季，这是一个非常有用的项目，而且[绅士制造者]已经足够友好地在 particle . io 上分享代码。如果这还不够好，[也许你可以把你的伞当作 WiFi 天线](https://hackaday.com/2018/04/28/umbrella-and-tin-cans-turned-into-wifi-dish-antenna/)。休息后的视频。

 [https://www.youtube.com/embed/dJhLOX_JbA0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/dJhLOX_JbA0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

