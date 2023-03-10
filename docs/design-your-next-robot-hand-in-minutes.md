# 在几分钟内设计你的下一个机器人手

> 原文：<https://hackaday.com/2022/06/23/design-your-next-robot-hand-in-minutes/>

麻省理工学院抱怨说，设计一只机器人手非常耗时，需要多次迭代。他们想通过给[一个模块化的手触觉传感器](http://robohands.csail.mit.edu)来改善这种情况。他们声称，对于许多实际应用来说，这可以将设计时间减少到几分钟。比如剪纸。你可以在下面看到关于这篇论文的视频，也可以阅读[的正文](https://arxiv.org/pdf/2204.07149.pdf)。

每种类型的操纵器都有一个关联的图形。预定义元素允许您组合手掌和专用手指。你使手指变形以匹配手的使用。然后一个看起来像手套的传感器为任务提供反馈。

所有这些的输出是 STL 文件，用于打印手和自动生产传感器连指手套的针织机图案。视频中的一些例子显示手臂操作剪刀，拧紧蝶形螺母，以及——对机器人手臂的经典测试，拿起鸡蛋。他们还展示了一个机器人从一个瓶子里倒液体，尽管有人必须先拿掉瓶盖来帮助它。

手指关节包括几个指尖和关节。图表显示了哪些部分可以相互连接，就像编译器知道数学表达式中的数字后面可能跟什么一样。变形过程也意识到了 3D 打印机的局限性，所以它产生了实用的形状。

你希望机器人手做什么？有了右臂，他们可以让你的 3D 打印笔最终派上用场。或者[接手你的焊接](https://hackaday.com/2019/04/26/3d-printer-becomes-soldering-robot/)杂务。然而，我们想知道是否会有新的机器人第四定律？不要拿着剪刀跑。

 [https://www.youtube.com/embed/UeusUSV6ios?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/UeusUSV6ios?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

