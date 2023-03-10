# 棍子上的 433

> 原文：<https://hackaday.com/2020/06/27/433-on-a-stick/>

廉价的 433 MHz 无线开关是进入家庭自动化世界的诱人方式，但如果没有专用硬件，它们就不太容易从 PC 上控制。这就是[TheStaticTurtle]所处的位置，所以解决方案是显而易见的。[搭建一个 USB 433 MHz 收发器](https://blog.thestaticturtle.fr/open433-lets-turn-light-on-with-the-computer)。

在计算机端是一个 CH340 USB 转串行芯片和熟悉的 ATmega328，使它成为 Arduino 的一个紧凑副本。在射频端是一对发射和接收模块，出人意料的是，它们具有独立的天线。该设备是第二次修订，在最初的实验中，一个天线连接器和一个射频开关被证明无效。在软件方面，Arduino 使用[RC-switch 库](https://github.com/sui77/rc-switch)，而在 PC 方面，有一个 Python 库来理解这一切。代码和硬件文件[都在 GitHub](https://github.com/TheStaticTurtle/Open433) 上，如果你想尝试的话。

制造单天线收发器的问题不适合胆小的 RF 工程师，因为虽然二极管开关在理论上似乎可以交付货物，但要做到正确并保持线性度可能极其困难。我们很好奇为什么没有使用收发器模块，但我们猜测成本在这个等式中起了重要作用。

多年来，我们已经推出了不少引人入胜的 433 MHz 项目，[比如这个 TP-Link 路由器转换](https://hackaday.com/2016/10/26/converting-a-tp-link-router-to-mission-control-for-cheap-433mhz-home-automation/)。