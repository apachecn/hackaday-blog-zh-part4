# 手势控制没有花哨的传感器，只有锅和重量

> 原文：<https://hackaday.com/2018/09/29/gesture-control-without-fancy-sensors-just-pots-and-weights/>

[丹尼斯]旨在通过抛弃操纵杆和按钮，使用无线手势控制来取代它们，使机器人控制更加直观。令人好奇的是，在他的[掌力中没有任何加速度计或陀螺仪！](https://hackaday.io/project/160350)项目。

手势检测不是由一个花哨的 IMU 组成，而是由两个电位计(每个轴一个)组成，轴上附有偏置配重。当手倾斜时，重物转动花盆的轴，产生的读数被转换成动作命令并通过蓝牙发送出去。这种设计当然有其所见即所得的一面，从整体上看，它的工作方式很像一个倒置的、加重的操纵杆挂在一个人的手掌上。

这是一种经济的方式来玩运动感测的想法，当谈到原型制作时，能够测试一个概念，同时保持成本最低是一个很好的技能。

The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)