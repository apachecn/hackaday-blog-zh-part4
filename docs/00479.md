# 这是树莓派机器人击败所有其他人

> 原文：<https://hackaday.com/2018/08/29/this-is-the-raspberry-pi-robot-to-beat-all-others/>

在树莓派问世之前，制造机器人很难。在底盘上转动马达的最佳解决方案是重新利用旧的 roomba。对于大脑来说，也许你可以把 Linux 放在路由器上，用旧的 Linksys 移动你的漫游者。在此之前，你可以买一个蹩脚的机器人套件，扔在一个盒子里，作为“教育套件”出售。我肯定有一些读者通过电线包裹 HC11s 来制造机器人。

现在我们有了 3D 打印机和树莓派，随之而来的是机器人技术的黄金时代。最好的机器人大脑之一是来自[Tim Wilkinson] 的 [8BitRobots 模块，这是今年 Hackaday 奖的参赛作品。](https://hackaday.io/project/152729-8bitrobots-module)

8BitRobots 模块由几个组件组成，其中最重要的是 Pi Zero，这是一台功能极其强大(就其价格而言)的 Linux 计算机，售价 5 美元。通过一个巧妙命名为 RoBonnet 的附加板，Pi Zero 可以获得伺服系统和 ESC 的 PWM 输出，电机的 H 桥，TTL 串行，编码器输入，压力和温度传感器，IMU，电源监控器，以及成功的 Pi 机器人所需的一切。

但是硬件只是等式的一部分。如果你想给一个机器人编程，你需要一个能让一切变得简单的软件栈。这就是 8BitRobots 分布式机器人平台的用武之地。这是一点运行在 Pi 上的 Javascript，允许你对机器人进行块状编程，这是一个类似 Scratch 的图形编程环境，适合在网络浏览器上运行。这是一个机器人开发和编程的一体化解决方案，也是今年 Hackaday 奖的一个出色补充。

The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)