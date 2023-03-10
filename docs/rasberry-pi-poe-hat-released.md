# 树莓派 poe 帽子发布

> 原文：<https://hackaday.com/2018/08/26/rasberry-pi-poe-hat-released/>

它是在三月初宣布的，但是现在树莓 Pi 以太网供电(PoE)已经上市了。由于在 Raspberry Pi 3 型号 B+上添加了一个新的 4 针接头，如果您已经设置好提供 PoE，Pis 可以从以太网电缆获得电源。

这是一项了不起的工程，尽管它只是通过以太网给一台小型单板计算机增加电力。从机械上来说，PoE 帽子根本不会增加树莓派的 3D 包围盒体积。它通过控制 I2C 上空的风扇来增加冷却效果。更奇怪的是，变压器被安装在一个印刷电路板上，我们非常想知道它是如何被指定、设计和组装的。是的，它可能只是树莓派的一个附加组件，但它的设计中有一些巧妙的工作。

[![](img/b8bf798951504cec6a1caffa0ff530c3.png)](https://hackaday.com/wp-content/uploads/2018/08/poe.jpg) 树莓 Pi 获得了 PoE 功能[去年 3 月](https://hackaday.com/2018/03/14/raspberry-pi-gets-faster-cpu-and-better-networking-in-the-new-model-3-b/)推出了树莓 Pi 3 Model B+,该版本确实需要对树莓 Pi 的硬件和引脚进行细微的更改。与 Pi 3 B 型相比，Pi 3 B+型在以太网插孔和一个安装孔旁边有一个四针接头。这是在 Pi 3 Model B 中发现的“Run”标题的相同位置，可能会让任何制作帽子以利用 Pi 上的真正电源按钮的人感到非常惊愕。

然而，木已成舟，现在我们有了一个真正的覆盆子 Pi PoE 解决方案。这对于任何想要构建 Raspberry Pi 集群计算机的人，或者任何正在将一些 Pi 放入已经有 PoE 硬件的服务器机架的人来说，都是一个福音。

你可以花 20 美元从常见的嫌疑人(Farnell，RS，[和其他经销商](https://www.raspberrypi.org/products/poe-hat/))那里买到一顶 PoE Pi 帽子。