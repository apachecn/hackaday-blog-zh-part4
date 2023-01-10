# DIY 自动卷帘

> 原文：<https://hackaday.com/2020/12/05/diy-automated-roller-blinds/>

使用现成的解决方案控制百叶窗可能会非常昂贵，如果您想要控制多个百叶窗，成本会更高。[HumanSkunk87]觉得成本太高，于是他们设计了一个控制器[自动打开和关闭百叶窗](https://imgur.com/a/xuQjH3z#lfxzUPm)。

这个建筑的主要部分是一个马达和一个球链齿轮——一个可以抓住球链的球的轮子，这样就可以拉动球链。轮子是用 Fusion3D 设计的，然后打印出来。马达需要足够的动力来拉动链条——[human skunk 87]计算出它需要能够拉动大约 2.5 千克才能升起百叶窗。在放弃步进电机后，人们发现带有蜗轮的 DC 电机有足够的扭矩工作。WEMOS D1 迷你控制电机控制器，驱动球链轮。两个微型开关告诉 WEMOS 何时停在窗口的底部和顶部。

WEMOS 使用 ESPHome 编程，并连接到[HumanSkunk87]的 HomeAssistant 以完成自动化。查看链接中对部件的描述和用于运行一切的代码。还有许多其他的[创造性的方法来打开你的百叶窗](https://hackaday.com/2020/08/19/automating-mini-blinds-the-rental-friendly-way/)，甚至有可能[自动窗帘代替百叶窗](https://hackaday.com/2019/10/14/the-morningrod-wants-your-mornings-easier-not-harder/)。

> [查看 imgur.com 的帖子](https://imgur.com/POZn2RO)