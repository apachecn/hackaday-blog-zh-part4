# PiSquare 允许你在一个树莓 Pi 上运行多个帽子

> 原文：<https://hackaday.com/2022/04/13/pisquare-lets-you-run-multiple-hats-on-a-raspberry-pi/>

Raspberry Pi 古老的 40 引脚接口和相关的 HAT 生态系统为平台带来了好处。将额外的硬件叠加到 Pi 上很容易，在某些情况下甚至可以多次叠加。然而，如果你想同时使用多顶帽子，而且是无线的，PiSquare [可能就是你想要的。](https://hackaday.io/project/184660-9-pisquare-can-connect-multiple-hats-wirelessly)

PiSquare 由一块包含 RP2040 和 ESP-12E 微控制器的电路板组成。它与 Raspberry Pi HATs 接口，甚至允许您在单个 Raspberry Pi 上运行多个相同的 HAT，因为它实际上并不直接使用主机 Pi 本身上的 UART、SPI 或 I2C 接口。相反，PiSquare 与 Pi 进行无线通信，用 HAT 本身处理 IO。

目前还不清楚这在软件层面上是如何工作的。对于一个给定的 Raspberry Pi，简单地使用现有的软件工具和库可能无法与 wireless PiSquare 设置一起工作。然而，对于高级用户来说，它可能有一个有用的目的，允许一个 Raspberry Pi 命令多个帽子，而不用担心必须运行更多的单板计算机，而一台计算机就可以了。对该设备感兴趣的人将可以在 Kickstarter 上获得电路板。

我们已经看到了树莓派和帽子系统的其他创造性的东西。[如果你一直在为这个平台设计你自己的整洁的程序，给我们写封短信吧！](http://hackaday.com/submit-a-tip)