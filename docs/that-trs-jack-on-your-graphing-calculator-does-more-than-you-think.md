# 图形计算器上的 TRS 杰克比你想象的要多

> 原文：<https://hackaday.com/2018/09/25/that-trs-jack-on-your-graphing-calculator-does-more-than-you-think/>

不是苹果 IIs，也不是树莓 Pis。教授儿童编程最重要的计算平台是德州仪器图形计算器。这些东西已经以这样或那样的形式存在了近三十年，对于许多初露头角的黑客来说，这是他们拥有的第一台计算机，并且可以完全访问它。

由于破解图形计算器是创客大会的最爱，我们很高兴看到 Cemetech 上周末在纽约举行的今年的世界创客大会上脱颖而出。他们是将这些显示屏非常糟糕的掌上电脑转变为可用计算平台的主要驱动力。

正如你在任何一个展台所期待的那样，Cemetech 展示了图形计算器的确切功能。最令人印象深刻的，至少从焊接的角度来看，是由图形计算器控制的 LED 立方体。电子设备很简单，只有几个 595 和晶体管，但这个 LED 立方体直接从图形计算器的连接线上获取串行数据。当然，LED 立方体的 PCB 被设计成 Arduino 屏蔽，以便于原型制作，但不要搞错:这是一个由计算器控制的 LED 立方体。

 [![IMG_20180923_120431](img/2096cde936f79456f8c45f688f41fbed.png "IMG_20180923_120431")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/09/img_20180923_120431.jpg?ssl=1)  [![IMG_20180923_120634](img/b94154800c60ff5708dfe0050ac305d7.png "IMG_20180923_120634")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/09/img_20180923_120634.jpg?ssl=1)  [![IMG_20180923_120739](img/339874bad2fb818a5607aa5b36fccf1f.png "IMG_20180923_120739")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/09/img_20180923_120739.jpg?ssl=1)  [![IMG_20180923_120749](img/a4a4678d16760436b3a6a31522ab6a16.png "IMG_20180923_120749")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/09/img_20180923_120749.jpg?ssl=1) 

如果您可以将串行数据从图形计算器发送到移位寄存器，这意味着您可以将串行数据发送到任何东西，从而将我们带到 Cemetech 今年的下一个伟大构建。这是一辆 N 轨距模型火车，完全控制机车。

如今，控制模型火车不仅仅是简单地将一个大的自耦变压器连接到轨道上。这种设置使用直接司机室控制(DCC)，这是一种调制机车命令的系统，同时仍向轨道提供 12-15V 电压。有一个很好的 Arduino 库，当你有了它，你可以很容易地把它移植到一个图形计算器。

Cemetech 是 Maker Faire 的常年最爱之一，多年来，我们已经看到了从配备 RGB 背光和 PS/2 端口的终极 TI-83+ 到图形计算器游戏 Whac-A-Mole 的[。这是一个很好的例子，说明你可以用每一个 90 年代的孩子都有的可编程计算机*做什么，也是对计算机编程教育的介绍，这是 Cemetech 正在努力推动的事情。*](https://hackaday.com/2016/01/25/the-newest-graphing-calculator-game/)