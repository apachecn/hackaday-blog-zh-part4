# 双有刷电机控制器不关心它如何接收命令

> 原文：<https://hackaday.com/2018/07/18/dual-brushed-motor-controller-doesnt-care-how-it-receives-commands/>

简单的 DC 有刷电机是许多机器人项目的核心。要制造在房子里跑来跑去的小玩具机器人，没有什么比一对有刷电机的价格和简单性更好的了。它们也很容易控制；你可以用分立晶体管制作自己的 H 桥，或者选择 L298N 或 L9110S 等常用 IC。

![](img/58818f835171cd5dd6c8e66f28c9bb83.png)

但是如果你想要一个一体化的解决方案呢？它能为大多数应用提供足够的电流，驱动双电机，并处理各种输入电压。最重要的是，它能与任何类型的输入源对话。作为他的 Hackaday 奖参赛作品，[Praveen Kumar]正在创造一种能够处理多种输入类型的双刷电机控制器。无论您使用的是 IR 遥控器、通过 I2C 通信的 Pi、模拟输出还是蓝牙接收器，该驱动程序都可以处理它们，并会自动选择正确的输入源。

该板有一个 ATmega328p 大脑，因此 Arduino 兼容性很容易在需要时重新编程。安装孔和头部位置也便于与 Pi 堆叠，还有一个状态 LED。这是一个很棒的模块，可以很容易地在很多构建中找到位置。

如果你需要对你的有刷电机进行更多的控制，你可以通过增加一个 PID 回路来增强它的能力。

The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)