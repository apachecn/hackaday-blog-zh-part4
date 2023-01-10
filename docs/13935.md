# 沃尔沃 C30 定制仪表和 CAN 总线逆向工程

> 原文：<https://hackaday.com/2022/06/15/volvo-c30-custom-gauge-and-can-bus-reverse-engineering/>

由于汽车本质上是有轮子的公共汽车，难怪在这些公共汽车上有许多关于汽车状态的有趣信息。主要问题通常是如何访问这些信息，包括连接到相关的 CAN 总线，以及解码所使用的(专有)协议。对[Alex]来说幸运的是，解码与他的沃尔沃 C30 一起使用的沃尔沃 VIDA 协议相对简单，使[能够创建一个定制的仪表](https://github.com/Alfaa123/Volvo-CAN-Gauge)，显示增压压力和冷却液温度等信息。

物理接口是通过汽车的 OBD 端口完成的，该端口方便地提供对汽车的两条(高速和低速)CAN 总线的访问。选择的硬件是一个[M2·UTH](https://www.macchina.cc/catalog/m2-boards/m2-under-hood)(引擎盖下)板，配备一个基于 SAM3X Cortex-M3 的 MCU，设计用于永久性汽车安装。在[Alex]的 GitHub 项目页面上，解释了协议如何工作，以及在复制项目时要寻找哪些字节。

完成这个项目的是一个来自 4D 系统公司的圆形 LCD 显示屏，它可以在状态更新屏幕上循环显示。此外，仪表盘的照明水平也是实时读出的，因此显示器的亮度被调整到适合这个水平。总的来说，这是一个全面的项目，有着将仪表更永久地集成到仪表板本身的有趣前景。

 [https://www.youtube.com/embed/kRip9_HPZf4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/kRip9_HPZf4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

