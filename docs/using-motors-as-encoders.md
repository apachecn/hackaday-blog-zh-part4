# 使用电机作为编码器

> 原文：<https://hackaday.com/2018/09/13/using-motors-as-encoders/>

如果你有一个无刷电机，你有一些磁铁，一堆线圈排列成一个圆圈，理论上，所有的零件，你需要建立一个旋转编码器。很多人使用无刷或步进电机作为旋转编码器，但他们似乎都是通过将电机用作发电机并查看相位和电压来实现的。对于他们的 Hackaday Prize 项目，[besenyeim] [正在以不同的方式进行](https://hackaday.io/project/160585-motor-as-encoder):他们使用电机作为耦合电感，看起来这是一种将电机转变为编码器的可行方法。

本项目的实验装置是基于 STM32F103 的 Blue Pill 微控制器。这与一组用于驱动电机的半桥相结合，实际上是旋转电机和检测电机*在哪里*唯一需要的东西。该电路利用六路数字输出驱动半桥的高端和低端，三路模拟输入用作反馈。最终的波形图看起来像三个彼此不同相的奇怪阶梯，通过正确的处理，这足以检测电机的位置。

目前，该项目旨在通过串行向微控制器发送命令，并让电机旋转到特定位置。不，这不是一个完全闭环控制方案来转动电机，但它实际上没有那么糟糕。未来的工作是将这些电机变成触觉反馈控制器，尽管我们确信有一些树莓 Pi 机器人会喜欢电机中的里程表。你可以看看下面的视频。

 [https://www.youtube.com/embed/yLl8YYMC-Kw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/yLl8YYMC-Kw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)