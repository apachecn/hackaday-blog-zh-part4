# Arduino 中的无零件温度传感器

> 原文：<https://hackaday.com/2019/02/26/the-no-parts-temperature-sensor-in-your-arduino/>

水下数据记录器 Cave Pearl project 的创始人[Edward]需要一种用微控制器测量温度的方法。通常，这个问题最容易解决的方法是在 I2C 公交车上安装一个温度传感器——这些传感器既便宜又容易买到。这与在 Arduino 中连接温度传感器无关。[这个构建是关于在你的时钟](https://thecavepearlproject.org/2019/02/25/no-parts-temperature-measurement-with-arduino-pro-mini-to-0-005c-or-better/)中使用温度传感器。

ATMega328p 是所有 Arduino Uno 克隆产品的核心芯片，它内部有一个看门狗定时器，以 110 kHz 的速率点击。这个看门狗定时器对温度有些敏感，通过测量这个温度传感器，您可以了解现代微控制器环氧树脂滴的温度。诀窍是校准看门狗定时器，这是通过冰箱中的自制“校准盒”来完成的，冰箱由两个非常重的陶瓷罐组成，中间有一袋大米来增加热量(你不能用水来做这件事，因为你把它放在冰箱里，古董罐子有点价值)。

通过反复让微控制器经历几次冻融循环，[Edward]能够将这个看门狗定时器校准到约 0.0025°C 的分辨率，这对于任何传感器应用都绰绰有余。尽管存在准确性和精确性的讨论，但这已经很不错了。

这种技术测量微控制器的温度，精度为 0.005°C 或更高，并且只使用中断定时器。这并不是说这是测量 ATMega 温度的唯一方法；这些芯片中的一些内置了温度传感器，[，我们在](https://hackaday.com/2014/02/01/atmega-attiny-core-temperature-sensors/)之前已经看到了使用这种传感器的项目。然而，数据手册中明确记载的这一特性似乎并没有被很多人使用。

感谢[jan]发送此邮件。