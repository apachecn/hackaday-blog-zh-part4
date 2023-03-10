# Joulescope DC 能量分析仪综述

> 原文：<https://hackaday.com/2019/03/06/joulescope-dc-energy-analyzer-reviewed/>

[VoltLog]获得了一个预发布的 [Joulescope](https://www.youtube.com/watch?v=0WU2eLBHXLo) 单元，这是一个 DC 能量分析器，它承诺使优化您的电子设计的功率和能量使用变得容易。你可以在下面的视频中找到他的评论。该设备是一个非常快速的电流表和电压表。考虑到这一点，很容易计算能量，以及随着时间的推移，功率。

根据视频中的一封信，这款设备的零售价约为 400 美元，尽管网站提到的价格接近 800 美元。对于一个实际上只是一个快速模数转换器和一些软件的专业设备来说，这两者似乎都有点多。公平地说，该器件可以读取 18 微安至 10 安的范围，分辨率低至 1.5 纳安。值得吗？这将取决于你的应用和你的价格敏感度。

该设备有香蕉插头，但也设置为处理带有一些适配器的 USB 设备。前面板实际上是一个带有连接器的 PCB，因此面板可以根据不同的应用而改变。该软件在通用平台上运行，并提供伏特计式视图和示波器式视图。电流范围越小，带宽越低，范围从 15 kHz 到 250 kHz。这不是一个范围的替代品，而是用来测量 DC 尖峰。[VoltLog]指出，当设备处于睡眠模式时，您最感兴趣的是低范围读数，因此较低的带宽应该不是一个大问题。

工作演示使用仪器附带的测试 Arduino 进行审查。换句话说，如果你买了其中的一个，它不会有示例板。您可以在软件中清楚地看到事件，如结果轨迹中的 LED 闪烁。

我们已经看到像这样的仪器[内置在 ESP8266 设计](https://hackaday.com/2018/02/28/monitor-power-consumption-of-low-power-devices/)中。我们也看到人们[用相当简单的技术测量微小的电流](https://hackaday.com/2016/02/01/need-a-nano-ammeter-you-already-have-one/)。

 [https://www.youtube.com/embed/0WU2eLBHXLo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/0WU2eLBHXLo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

