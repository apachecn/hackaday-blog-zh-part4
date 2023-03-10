# 2022 年网络平台竞赛:Galdeano 不仅仅是一个图形计算器

> 原文：<https://hackaday.com/2022/09/15/2022-cyberdeck-contest-the-galdeano-is-more-than-a-graphing-calculator/>

图形计算器已经从富裕书呆子的昂贵玩物演变成全世界高中生的日常工具。尽管现在的青少年口袋里装着功能强大的联网电脑，但数学老师通常更喜欢他们在课堂上使用笨重的 Z80 计算器，只是因为他们有限的性能降低了分心的可能性。一个懒惰的学生能做的最糟糕的事情就是玩一个简单的游戏，比如*蛇*或者*俄罗斯方块*。

但是，如果您不再是学生，而是想要一个拥有最新硬件和无限软件定制能力的图形计算器，该怎么办呢？看看[Angel Cabello]的 [Galdeano 就知道了，这款掌上电脑拥有现代图形计算器的所有功能，还多了很多](https://hackaday.io/project/187213-galdeano-handheld-computer)。该设备的核心是一个 ESP32，它位于一个定制的 PCB 上，PCB 上还有一个 6×7 的按钮阵列和一个 320×240 的触摸敏感彩色显示器。它可以通过锂聚合物电池供电，或者像经典计算器一样，通过四节 AAA 电池供电。整个东西都装在一个 3D 打印的外壳中，带有彩色编码的按钮，指示各种内置功能。

ESP32 运行 MicroPython 和一个名为 Eigenmath 的符号数学引擎。这使得 Galdeano 能够操作表达式，执行积分和微分，以及绘制函数。将 Eigenmath 移植到像 ESP32 这样内存受限的平台上是一个相当大的挑战，需要一些变通办法，包括内存分区方案，甚至是带有数学符号的定制紧凑字体。

由于 MicroPython 和 ESP 的 WiFi 系统的灵活性，Galdeano 不仅限于实现计算器:它还可以执行各种通用任务，从文件编辑到控制一组智能灯泡。项目页面还没有提到任何游戏，但我们确信不久之后就会有人把俄罗斯方块移植到这个系统上。

当然，即使是教室级别的计算器也可以做比设计者预想的更多的事情:它们可以[接收 GPS 信号](https://hackaday.com/2014/02/04/gps-for-a-graphing-calculator/)，[运行 Debian](https://hackaday.com/2014/11/18/running-debian-on-a-graphing-calculator/) ，甚至[执行光线追踪](https://hackaday.com/2022/02/21/ray-tracing-on-a-modern-ti-graphing-calculator/)。如果你正在寻找一个强大的开源计算器，这个基于 BeagleBoard 的机器运行 R 统计计算环境。

 [https://www.youtube.com/embed/HeJPX-fPN6Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/HeJPX-fPN6Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[![Hackaday.io Cyberdeck Contest](img/44f5c5a520ce0ee08b0944485b6874a1.png)](https://hackaday.io/contest/186672-2022-cyberdeck-contest)