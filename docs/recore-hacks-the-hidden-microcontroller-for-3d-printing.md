# Recore Hacks 为 3D 打印隐藏的微控制器

> 原文：<https://hackaday.com/2021/06/14/recore-hacks-the-hidden-microcontroller-for-3d-printing/>

对 3D 打印机世界并不陌生，[智能代理]工作室的[Elias Bakken]发布了一款名为 Recore 的新[控制板。典型的 3D 打印机有一个专用控制器，处理驱动步进电机的实时方面。许多设置还有第二台计算机，通常基于 Linux，专门用于支持运行 Octoprint 服务器和连接数码相机以远程监控打印进度等任务。[Elias]的设计将这些融合在一个紧凑的 12 x 12 x 4 cm 封装中。](https://www.iagent.no/2021/06/04/recore-is-finally-printing/)

![](img/ca5cbff24a8f23d43d3a82d39910d6ab.png)

Recore 板由一个 [AllWinner A64 片上系统(SoC)](https://linux-sunxi.org/A64) 驱动，它包含四个运行 Debian Linux 的 ARM Cortex-A53 AArch64 内核。这些应用包括 [Klipper](https://www.klipper3d.org/) ，一个我们[在](https://hackaday.com/2017/12/26/fast-3d-printing-with-raspberry-pi-but-not-how-you-think/)刚推出时写过的项目，以及 [OctoPrint](https://en.wikipedia.org/wiki/OctoPrint) 打印服务器。“但 Linux 不是实时操作系统”，我们听到你哭了，“从 A64 SoC 控制步进电机驱动器只是自找麻烦”。[Elias]本来可以通过在电路板上放置一个辅助微控制器来解决这个问题，但他找到了一个更优雅的解决方案。

![](img/b42a21c97a2ec81d519c4190b47f3d08.png)

事实证明，A64 本身已经集成了一个隐藏在众目睽睽之下的次级微控制器。看到框图顶部标有 *AR100* 的小方框了吗？来认识一下 [AR100](http://linux-sunxi.org/AR100) ，这是一个原本用于管理 A64 低功耗运行的控制器。它是一个 [OpenRISC](https://en.wikipedia.org/wiki/OpenRISC) 32 位[或 1k](https://openrisc.io/architecture) 处理器。但 AR100 的利用率极低，[Elias]很好地利用了这一点，将其重新用于与 3D 打印机控制器相关的实时任务。观看下面的短片，了解他如何解决一些基本的实现细节，如定时器和与 Linux 处理器的通信。您可能会从本系列的其他短视频中学到一些技巧，这些视频展示了一些有趣的调试和问题解决会话。有一个项目 [GitHub 知识库](https://github.com/intelligent-agent/Recore)和一个 [Wiki](https://wiki.iagent.no/wiki/Recore) 充满了好的信息和测试结果。

[Elias]在构建打印机控制器方面有着悠久的历史。虽然他的最后一个因为制造问题不得不放弃，但他从那次经历中吸取了教训。在 Recore 的设计中，可制造性是首要考虑的因素。我们嫉妒挪威设备完善的[智能代理]设施，但更嫉妒[埃利亚斯]似乎喜欢的游牧生活方式——在他的视频中，可以看到他在遥远的地方工作，如热带岛屿度假村和漂浮在高地球轨道上的实验室。我们在过去展示过[Elias]的项目，包括[复制 3D 打印机控制器](https://hackaday.com/2018/03/25/turning-the-beaglebone-on-a-chip-into-a-3d-printer-controller/)、[半自动酒柜](https://hackaday.com/2017/08/18/latskap-semi-automatic-liquor-cabinet/)和[狗操作的零食分配器](https://hackaday.com/2017/07/27/dog-operated-treat-dispenser/)。

 [https://www.youtube.com/embed/Q5tIKX7jtCA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Q5tIKX7jtCA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

