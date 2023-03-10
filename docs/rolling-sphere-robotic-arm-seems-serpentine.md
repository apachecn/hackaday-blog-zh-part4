# 滚动球体机械臂看起来蜿蜒曲折

> 原文：<https://hackaday.com/2022/09/01/rolling-sphere-robotic-arm-seems-serpentine/>

铰链关节通常是机器人应用中最简单的，但如果您想要运动看起来更有机，滚动关节(或滚动接触)机制值得一看。[Skyentific]正在试验这种机制，[用它建造了一个 6 自由度的机械臂](https://www.youtube.com/watch?v=tcDDDaSMW0I)。

该机制不一定需要物理表面相互滚动才能工作，通过虚拟滚动球体机制，您可以获得两个自由度。[Skyentific]演示了这些如何与纸板剪纸和 3D 打印模型一起工作。将三个这样的机械装置堆叠在一起，每个阶段由三个 Dynamixel 伺服系统驱动，运动看起来几乎是蛇形的。

由于伺服系统驱动着每一级的底部小连杆，它们在机械上处于明显的劣势。手臂在桌面上几乎无法保持直立，所以[Skyentific]将它倒置在桌子底部，以减轻其重量负荷。去掉了前级，负载明显减少，也没那么纠结了。

这种机制的一个有趣的优点是，总有一条笔直的布线路径。两块板之间的这条线的长度在整个运动范围内保持不变，因此它也可用于确定刚性驱动轴的路线。这实际上是在 [LIMS2-AMBIDEX 机器人](https://hackaday.com/2019/10/20/humanoid-robot-has-joints-that-inspire/)上做的旋转它的手，也是第一次看到这个机构的地方。有趣的是，这种实现本身并不驱动连杆机构，而是在机构周围使用张力索。我们在非常相似的[触手机器人](https://hackaday.com/2020/09/15/a-tentacle-thats-a-work-of-art/)中也看到了这一点，所以这可能是一个更好的选择。

 [https://www.youtube.com/embed/tcDDDaSMW0I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/tcDDDaSMW0I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

