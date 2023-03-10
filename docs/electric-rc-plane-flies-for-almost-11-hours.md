# 电动遥控飞机飞行近 11 小时

> 原文：<https://hackaday.com/2021/06/27/electric-rc-plane-flies-for-almost-11-hours/>

电动遥控飞机并不以飞行时间长而闻名，多旋翼飞机通常飞行 20-45 分钟，而大多数固定翼飞机将努力超过两个小时。马修·海斯凯尔用电池驱动的遥控飞机进行了 10 小时 45 分钟的飞行。休息后的浓缩视频。

![](img/c095c7bfe7a7ebc81f865e95b75c33a5.png)

Flight stats right before touchdown. Flight time in minutes on the left, and miles travelled second from the top on the right.

秘密？高效的飞机，良好的自动驾驶仪和巨大的电池。[Matthew]使用 LG 21700 电池打造了一个定制的 4S 50 Ah 锂离子电池组，重量为 2.85 千克(6.3 磅)。机身是凤凰 2400 电动滑翔机，翼展 2.4 米，由 600 [Kv](http://learningrc.com/motor-kv/) 无刷电机驱动，转动 12 x 12 螺旋桨。30 A 电子稳定控制系统的低电压切断功能被禁用，以确保电池的每一点能量都可用。

为了提高效率，消除马拉松飞行中保持手动控制的需要，增加了 GPS 和 Matek 405 机翼飞行控制器，运行 ArduPilot。ArduPilot 离即插即用还很远，所以[马修]将不得不花费大量时间调整和测试参数，以获得最大的飞行效率。我们真的很好奇，看看是否有可能通过改善突出电池周围的空气动力学来进一步延长飞行时间，增加一个皮托管传感器来保持升阻曲线上的完美空速，并可能通过 [ArduPilot 的新飙升功能](https://ardupilot.org/plane/docs/soaring.html)利用热气流。

你们中的一些人可能在想，“太阳能电池板！”，马修也是。他还有另一副翅膀，他曾用它来做 7 小时的飞行。虽然理论上它应该增加飞行时间，但他发现有许多明显的缺点。除了增加重量、电气复杂性和天气依赖性之外，太阳能电池很难在不降低空气动力学效率的情况下集成到机翼上。考虑到我们已经看到的【rcflightest】的各种[实验/与](https://hackaday.com/2019/10/09/soaring-with-the-sun-4-years-of-solar-rc-planes/)[太阳能飞机](https://hackaday.com/2021/05/29/solar-plane-is-like-one-big-flying-solar-panel/)的斗争，我们开始怀疑是否真的值得这么麻烦。

 [https://www.youtube.com/embed/HGZC-cvYcb8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/HGZC-cvYcb8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

