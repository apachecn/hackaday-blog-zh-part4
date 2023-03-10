# Arduino 支持多点触控

> 原文：<https://hackaday.com/2019/11/17/arduino-does-multitouch/>

现在很多消费电子产品都使用触摸传感器。这是一种廉价而可靠的方式来取代从耳机到汽车等一切东西上的各种旋钮和开关。然而，为一次性项目创建自定义触摸控制器可能会令人望而生畏。ACM 最近的一篇论文展示了[任何电容式传感器仅仅使用 Arduino 就可以作为多点触摸传感器](https://dl.acm.org/citation.cfm?doid=3332165.3347895)工作，尽管运行处理的 PC 会为更高级的功能解释数据。

关键是 Arduino 使用 PWM 激励电网，然后检查来自电网的信号。手指戳会大大改变响应，Arduino 可以使用板载的模数转换器来感知它。你可以在网上找到实际的[软件包。如果你只想使用工具包，教程](https://hci.cs.uni-saarland.de/multi-touch-kit/)[文档](https://github.com/HCI-Lab-Saarland/MultiTouchKitDoc/blob/master/MTK_Tutorial.pdf)可能比 ACM 论文更有趣。

最佳驱动频率为 10 MHz。这些示例依靠较低频率 PWM 信号的谐波来实现。模拟转换当然没有那么快，但由于你的手指触摸速度相对较慢，他们将信号视为调幅输入，非常容易解码。

传感器可以是导电墨水、线或铜带。有几个示例应用程序，包括一个你可以抚摸的 3D 打印兔子，一个袖子上的控制面板和一个交互式贺卡。

传感器形成图像，OpenCV 检测实际的触摸配置。看起来你也可以使用来自 Arduino 的原始数据，但是可能有点困难。

我们设想铝箔会与这种技术一起工作。如果你开始布置 PCB，[这可能会派上用场](https://hackaday.com/2013/12/04/easy-capacitive-touch-sensors-in-eagle/)。