# ESP32 土壤监测器进入超低功耗模式

> 原文：<https://hackaday.com/2021/01/14/esp32-soil-monitors-tap-into-ultra-low-power-mode/>

土壤湿度传感器价格低廉，易于使用，将一个传感器与 Arduino 结合起来，当你的盆栽植物感到有点干燥时，LED 就会闪烁，这是一个常见的初学者项目。但是从长远来看呢？除了简单的概念证明之外，在几周或几个月的时间里，从这些传感器中实际读取数据需要什么？

这正是[德弗洛]最近不得不回答的问题。目标是建立一个设备，使[能够轮询多个土壤传感器，并将数据无线推送至家庭助手](https://blog.m3k.cc/2021/01/ultra-low-power-soil-monitor/)。但是由于它将在外面的阳台上，它需要完全依靠电池供电。幸运的是，他选择的平台 ESP32 具有一些惊人的节能特性。你只需要知道如何使用它们。

[![](img/98586498fcd7b11d39e8e834b7859c0e.png)](https://hackaday.com/wp-content/uploads/2021/01/esp32soil_detail.jpg)

The custom board can read from six soil sensors.

在他极其详细的博客文章中，[derflob]回顾了一些他用来尽可能多的运行时间的技巧。最大的一个，也可以说是整个项目的关键，是他对 ESP32 的超低功耗协处理器(ULP)的使用。这种强大的功能允许微控制器做一些有用的工作，尽管指令集减少了，但不会唤醒耗电的主处理器。

由于 ULP 可以从 ADC 读取数据，因此他能够编写一些汇编代码，只有在自上次更新以来，六个相连传感器之一的读数变化超过设定阈值时，这些代码才会唤醒 CPU。这使得芯片大部分时间都处于休眠状态，到目前为止，[derflob]说他的电路板已经在单个 LiFePO4 18650 电池上运行了六个月。如果你不是那么热衷于汇编，我们已经看到了一个类似的技术，用一个简单的[电路完成，它只在有工作要做的时候唤醒微控制器](https://hackaday.com/2020/05/18/esp32-trail-camera-goes-the-distance-on-aa-batteries/)。

那么，这个项目将何去何从呢？现在 PCB 已经基本完成，[derflob]正在将注意力转向它和传感器的防水，这样它们就可以在户外的环境中生存。某种环氧树脂封装可能是有序的，尽管这将是另一天的项目。