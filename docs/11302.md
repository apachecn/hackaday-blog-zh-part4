# 深入研究 SPI

> 原文：<https://hackaday.com/2021/09/16/taking-a-deep-dive-into-spi/>

随着库的普及，与数百个不同的传感器、显示器和子模块进行通信变得前所未有的简单。但是，当您在 Arduino IDE 中键入 SPI.begin()时，实际发生了什么呢？[在他最近的视频](https://youtu.be/MCi7dCBhVpQ)中，【Ben Eater】探索了串行外设接口(SPI)及其实际工作原理。

大多数 Hackaday 读者可能从他基于试验板的计算机中了解[Ben]，例如我们在 2019 年介绍的 6502 版本。从那以后，他一直在努力工作，为他的试验板计算机添加新的有趣的东西，并深入研究不同的通信协议，以便更好地理解和实现它们。在这个视频中，[Ben]设定了将 BME280(一种带 SPI 接口的常见压力、温度和湿度传感器)连接到他的试验板 6502 计算机的目标。在这一过程中，[Ben]讨论了 SPI 的具体工作原理，以及在研究不同的 SPI 器件时为什么会有如此多的术语和操作冲突。

如果你不喜欢试验板电脑，BME280 还有很多其他用途，比如帮助卡西欧 F-91W 实现现代化。

 [https://www.youtube.com/embed/MCi7dCBhVpQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/MCi7dCBhVpQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

