# 使用 LiPo 电池组为 USB-C 设备充电

> 原文：<https://hackaday.com/2018/07/14/charging-usb-c-devices-off-of-lipo-battery-packs/>

当它在 90 年代末被引入时，USB 是所有计算中最伟大的成就。键盘和鼠标的 PS/2 连接器、ADB 端口、并行端口、游戏端口和串行端口都不见了。这是一个将所有港口统一在一个标准的通用总线下的巴别塔。

然后引入了更多的端口；微型的，迷你的，那种奇怪的是侧面有更多连接器的迷你 USB。然后我们开始使用手机充电器作为电源。巴别塔已经倒塌了。然而，现在有了未来。USB-C 就是把所有东西都塞进一个端口，它可以提供 100 瓦的功率。

通过 USB-C 连接器供电是一项有趣的工程挑战，对于他的 Hackaday 奖参赛作品，[Chris Hamilton]正在接受这项任务。他正在制作一个 USB-C 电池充电器，允许他通过 USB 为标准遥控电池组充电。

充电器有两个主要部件。第一个是 Cypress CCG2 USB 电源传输协商器，它处理向 USB 电源发送命令并告诉它打开管道的所有逻辑。这是一款现成的器件，其实现在应用笔记中有详细记录。第二个主要组件是 TI BQ40z60RHB 上构建的电池管理电路。这包括充电器控制逻辑和平衡多达四个电池的能力。电池连接器是 XT-30，所以你所有的无人机电池组现在都可以通过 MacBook 充电。

The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)