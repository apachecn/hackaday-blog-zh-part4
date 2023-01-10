# 一种简单的可编程灯光控制器

> 原文：<https://hackaday.com/2019/04/11/a-simple-programmable-light-controller/>

如今一切都联网了，车库门、婴儿监视器和厨房水槽都连在一起了。把所有东西都放在网上有好处，但也有几个陷阱。维护家庭网络的安全是一项持续的工作，必须跟踪的设备数量增加了这项工作的难度。有时候所有的麻烦都不值得，你只是想要一个非连接的解决方案。[Dilshan]发现自己就在那个营地里，[建造了一个简单的可编程灯光控制器，它不连接到互联网。](https://hackaday.io/project/164514-programmable-light-controller)

该项目的核心是一个 ATMEGA8 微控制器，它便宜，容易获得，可以完成这项工作。它与 DS1307 实时时钟 IC 相结合来记录时间。该电路设计用于 24V 电源，以允许它从与它设计控制的 LED 灯模块相同的电源运行。

该设计最初的原型是试验板上的通孔器件，最终的设计是在定制的 PCB 上使用表面贴装器件。灯光由 7W 暖白色 LED 模块提供。3 个按钮和一个 4 位数的 7 段显示器作为用户界面，LDR 允许光线对周围环境做出反应。

这是一个违背当前趋势的构建，缺乏 WiFi 连接、Twitter 功能或基于云的日志记录。这表明，正确的解决方案并不总是把所有东西都放在网上。有时老方法足以完成工作，而且做得很好。

当然，如果你仍然渴望一个数据包解决方案，这里有一些如何在互联网上闪烁的方法。