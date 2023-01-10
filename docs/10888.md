# 针对老龄汽车的定制组合仪表

> 原文：<https://hackaday.com/2021/08/01/custom-instrument-cluster-for-aging-car/>

在过去的几十年里，对车辆的所有技术改进已经导致了轿车和卡车，对于任何在 20 世纪 70 年代驾驶福特平托的人来说，这似乎是不可思议的。汽车不仅因为防撞缓冲区、防抱死刹车、安全气囊和强制使用安全带而变得更加安全，而且还有各种各样的传感器、用户界面和计算机也改善了驾驶体验。至少，直到它开始磨损。我们现代汽车中的电子技术可能很难更换，但[Aravind]至少能够[更换他的老化(但仍然现代)斯柯达上的部分仪表组](https://www.team-bhp.com/forum/diy-do-yourself/239199-diy-skoda-laura-custom-instrument-cluster-mfd-display.html),并在此过程中对其进行改进。

这些汽车有一个反复出现的问题，中央部分的集群，包括一个液晶显示器。即使能找到替换零件，它们的价格也只占汽车价值的很大一部分，对大多数人来说是不经济的。[Aravind]发现，一旦旧屏幕被移除，已经可用的 3.5 英寸彩色液晶显示器完全适合这个空间，因此接下来的步骤是将其连接到汽车上。它们有一条与主控制 CAN 总线分开的 CAN 总线，并且端口很容易访问，因此获得了一个带 RTC 的 Arduino 来处理与其接口的繁重工作。

现在，[Aravind]在控制台中有一个新的 LCD 屏幕，它是完全可编程的，可能比工厂 LCD 更持久。在项目页面上也有这个过程的完整文档，适用于这个时代拥有大众汽车的任何人。无论哪种方式，这都是一种比支付 OEM 替换零件的巨额成本更经济的更换模块的方法。当然，像这样的 CAN 总线黑客通常是做更复杂的 CAN 总线项目的门户项目，如将整辆车变成视频游戏控制器。

 [https://www.youtube.com/embed/kICtPTi6pFg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/kICtPTi6pFg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

