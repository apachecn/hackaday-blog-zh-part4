# 电子和 C++教育与态度 13

> 原文：<https://hackaday.com/2022/05/14/electronics-and-c-education-with-an-attiny13/>

当[Adam，HA8KDA]不忙于他的博士研究时，他指导一群对工程感兴趣的学生。为了教授他们广泛的话题，他着手[构建一个小型且有趣的嵌入式项目](https://github.com/kissadamfkut/mora_blinker)，让他们一路观看并参与其中。在这个 LED 装饰的 ATTiny13A 项目中，[Adam]演示了原理图和 PCB 设计，然后教授了 C++基础知识和复杂性——特别是在构建低占用空间的软件方面——并将其结合到学生可以在项目结束后带回家的真实设备中。他的课程远远超出了我们通常期望的“你好世界”，我们中的一些人只能希望有这样的大学经历。

他与我们分享了 PCB 文件和软件，但同时也谈到了他为此开发的 C++20 框架。ATTiny13A 非常便宜，也非常有限——你有 1K 的只读存储器和 64 字节的随机存取存储器。这个框架让您可以很好地利用它，提供了一些基本的东西，比如 GPIO 摆动，也提供了一些小功率操作挂钩、具有可选多相操作支持的软 PWM 和 EEPROM 访问。学生可以为这个设备编写自己的动画，他把它们包含在报告中，！

在教育项目中，保持代码直接、干净、简洁并易于学生使用是值得的。只有当你真正理解你正在使用的工具时，你才能实现这些事情，这是教授它们的最佳位置！[Adam]旨在表明 C++更适合低资源设备，并告诉我们他编写的 EEPROM 类代码——编译成与汇编实现相同数量的指令并消耗相同数量的 RAM，同时提供编译时检查和故障安全语法。

我们之前已经讨论过在微控制器上使用 [C++，在没有开销的情况下获得额外的编译时特性，这个项目很好地阐释了这个概念。[Adam]问我们所有人，尤其是我们的 C++奇才同事，对](https://hackaday.com/2017/05/05/using-modern-c-techniques-with-arduino/)[设计的框架有何看法。](https://github.com/kissadamfkut/mora_blinker/tree/main/sw)您能否用这个简单的硬件实现更多——让代码更加健壮、简洁，让它在有限的资源内做更多的事情？

你能用 ATTiny13 构建什么，尤其是用这样一个框架？也许是一个华而不实的可佩戴发夹，或者是一个 T2 的代码学习射频遥控插座。我们还看到了[一个用于耐力赛的微型相机触发器、](https://hackaday.com/2012/03/29/808-camera-hack-produces-a-time-lapse-tic-tac-box/)、一个[手持*Flappy Bird*-就像](https://hackaday.com/2011/06/26/attiny13-powered-handheld-helicopter-game/)控制台，以及[更多！](https://hackaday.com/tag/attiny13/)