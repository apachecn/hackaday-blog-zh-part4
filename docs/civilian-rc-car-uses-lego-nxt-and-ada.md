# 民用遥控车用乐高 NXT 和 Ada

> 原文：<https://hackaday.com/2020/03/14/civilian-rc-car-uses-lego-nxt-and-ada/>

早在上个世纪，美国国防部宣布 Ada 将被用于任何地方和任何事情。书籍出版了，学校建立了课程。然而，正在工作的程序员填写了弃权书，继续使用他们选择的语言工作。结果只有一点点安全关键的软件真正用上了 Ada。然而，我们注意到最近有一点复苏。典型的例子:[一辆用 Ada 做大脑的遥控汽车](https://blog.adacore.com/making-an-rc-car-with-ada-and-spark)。你可以在下面的视频中观看它的工具。

在过去的几个月里，这已经不是我们第一次听到关于阿达的消息了。部分地，这可能是因为 GNU 编译器的可用性，尽管它从 1995 年就已经存在了，所以可能有另一种解释。Ada 的强类型确实倾向于堵塞黑客利用的漏洞，所以虽然我们不愿意说它是防黑客的，但与许多流行语言相比，它确实是防黑客的。

这辆车看起来是一个有趣的项目。他们从乐高 NXT 开始，但更换了控制器。使用高科技设计给你一个运动基地，有阿克曼转向和驱动轮上的差异。最初的设计使用红外接收器与乐高遥控器通话，但 Ada 版本也增加了蓝牙连接。

对于替换的 CPU，一个 15 美元的发现板将一个运行在 168 MHz 的 Cortex M4 放在板上。一些第三方模块和 Altoid 罐中的一些零件完成了汽车的电子部分。

万一你错过了所有 Arduino 提供的库， [Ada 驱动库](https://github.com/AdaCore/Ada_Drivers_Library)提供了定时器、通信等接口。并不是汽车需要的所有东西都在库中，但是一些抽象使得创建和集成定制部件更加容易。

如果您曾经对 Ada 感兴趣，这是一个值得学习的有趣项目，复制起来也不会太难。如果你制造不安全的东西——大型机器人、无人驾驶飞机或可能做坏事的东西的控制系统——你应该考虑 Ada 作为减少潜在灾难的一种方法。

去年，玛雅·波什为阿达做了一个案例。如果你愿意，你甚至可以[瞄准 RISC-V](https://hackaday.com/2018/10/08/programming-a-risc-v-softcore-with-ada/) 。

 [https://www.youtube.com/embed/Hngzh5zDM3E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Hngzh5zDM3E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

