# 开放式割草机:带 RTK GPS 的开源机器人割草机

> 原文：<https://hackaday.com/2022/04/07/openmower-open-source-robotic-lawn-mower-with-rtk-gps/>

在一些地方，机器人割草机正在成为一种常见的景象，这是因为现代工程的发展速度大大降低了电机和所需控制电子设备的成本。但是，在许多情况下，它们看起来仍然相当愚蠢，只不过是用旋转的刀片顶起来了。[Clemens Elflein]采用了一台廉价、愚蠢的割草机，并在树莓 Pi 4 和树莓 Pi Pico 的基础上对它进行了大脑移植，以实现实时控制。[Clemens]将这个叫做[open mower](https://github.com/ClemensElflein/OpenMower)，动机是创建一个支持 GPS 导航的开源机器人割草机控制器，使用 RTK 获得额外的精度。

捐赠机器人是 YardForce Classic 500，在检查控制 PCB 后，看起来许多其他机器人割草机模型可能使用相同的控制器，因此与开放式割草机平台兼容。一个定制的主板容纳了 Pi 4 和 Pico，一个 [ArduSimple RTK GPS 模块](https://www.ardusimple.com/)(据报道导航精度为 1 厘米)，以及三个用于车轮和转子的 BLDC 电机驱动器。一切都基于模块，插入主板，大大降低了项目的复杂性。对于一个廉价的割草机平台，Yardforce 单元具有良好的构建质量，到处都有连接器，使 OpenMower 成为即插即用的解决方案。甚至割草机顶部的用户界面也是可用的，下面的定制 PCB 在适当的位置提供了一些按钮。

[![](img/5750d80caa6231635ff481fbea3771c0.png)](https://hackaday.com/wp-content/uploads/2022/04/openmower_detail.jpg)

OpenMower mainboard

电机控制由 [xESC 项目](https://github.com/ClemensElflein/xESC)提供，该项目通过串行链路与主机控制器接口，提供低成本的 FOC 电机控制。这本身就值得研究！在软件方面，[Clemens]正在使用 [ROS](https://github.com/ClemensElflein/OpenMower/tree/main/ROS) ，它实现了低级机器人控制、路径规划(使用来自 Slic3r 的代码)以及物体回避的运动学约束。下面的视频显示了该机器的操作有多简单——只需用手持控制器驱动它在草坪周围行驶，并向它显示树木等障碍物的位置，然后启动它。割草机甚至能够修剪多块草坪，使它们之间的旅程自动进行！

机器人割草机项目在这里并不新鲜，这里有一个有趣的神秘的 TK，另一个[使用 RTK GPS 做好事(或者可能是坏事)](https://hackaday.com/2020/08/16/draw-on-your-lawn-with-this-autonomous-mower-and-rtk-gps/)，很可能是我们已经见过的[最简的一个](https://hackaday.com/2020/01/10/diy-autonomous-mower-in-the-wild/)，它使用 LoRa 基站传输 RTK 校正。我们建议远离最后一个。

 [https://www.youtube.com/embed/BSF04i3zNGw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/BSF04i3zNGw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

