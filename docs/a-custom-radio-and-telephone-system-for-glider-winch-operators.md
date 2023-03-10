# 滑翔机绞车操作员用的定制无线电和电话系统

> 原文：<https://hackaday.com/2022/03/01/a-custom-radio-and-telephone-system-for-glider-winch-operators/>

虽然滑翔可能是在空中移动的最平静和和平的方式，但发射滑翔机是一个相当嘈杂和暴力的过程。虽然电动绞车确实存在，但大多数机场都使用大型 V8 引擎机器来让滑翔机升空。[Peter Turczak]注意到他的机场的绞车操作员经常不得不在按下按钮和移动操纵杆的同时改变多个通信频道，所有这些都伴随着他们旁边内燃机震耳欲聋的轰鸣声。为了让他们的生活更容易，他建造了一个单一的通信设备，结合了多个无线电输入和一个模拟电话。

[![A stack of circuit boards next to an old phone ringer](img/51f98e05c4dbe46503b63cfcc0b91ce5.png)](https://hackaday.com/wp-content/uploads/2022/02/Glider-winch-phone-inside.jpg)

The inside of the cabinet. Note the classic phone ringer

主用户界面是一个坚固的耳机，可以显著降低发动机噪音。这种耳机连接到一个机柜，机柜包含几个模块，连接到不同的音频源:模拟电话线，飞机无线电接收器，PMR 手持收音机，甚至在其他线路安静的情况下还有一个音乐源。该系统包含基于优先级系统的自动切换电路，确保重要消息不会错过。

电子设计基于 NE5532 和 TL084 运算放大器等经典模拟器件，全部安装在小型定制 PCB 上。音频变压器用于避免各种信号源之间的接地环路，而继电器则用于静音非优先信号源。为了确保与电话网络的无缝兼容，[Peter]使用了老式台式电话的组件，包括线路变压器、DTMF 键盘甚至机械振铃器。他在博客中发表了很多细节，任何从事运算放大器和音频工作的人都会对这些细节感兴趣，比如如何稳定输入端具有较大布线电容的放大器。

从本质上来说，整个项目“只是”一个混音器，尽管是为一个非常具体的目的而优化的。但是设计一个简单的混音器绝非易事，正如我们几年前报道的那样。如果你对绞盘更感兴趣，你会很高兴地发现，较小的绞盘也可以用于[滑雪橇](https://hackaday.com/2011/03/01/super-winch-makes-sledding-100-more-fun/)，甚至[滑水](https://hackaday.com/2010/10/05/build-a-beach-winch-for-wakeboarding/)。