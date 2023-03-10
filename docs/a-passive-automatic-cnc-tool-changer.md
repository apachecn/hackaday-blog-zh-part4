# 一种被动式自动数控换刀装置

> 原文：<https://hackaday.com/2022/06/25/a-passive-automatic-cnc-tool-changer/>

【马里乌斯·霍恩伯格】又在忙着黑他的“锤子”数控刳刨机了，现在它有了一个非常渴望的功能——一个[自动换刀装置](https://www.youtube.com/watch?v=ZeOUdosoEBM)。想要一个已经有一段时间了，[Marius]不乐意牺牲一大块可用的床面积来停放换刀盒。一个显而易见的解决方案是将杂志收回远离床，在工作区之外。遗憾的是，CNC 控制器只有足够的备用输出来驱动气动换刀装置(安装在主轴上)，没有多余的输出来控制料盒组件。因此，只有一个显而易见的途径，使用一些简单的弹簧加载的机制，以 Y 轴运动将杂志移动到刀具拾取范围。

显然，整个事情是在机器本身上数控加工的，只需要几次迭代和少量的台锯动作，就可以让一切都很好地适应和平稳运行，而不会与移动的门架绑定或碰撞。在料盒的每一端都有一对巧妙的杠杆，允许它比前进的机架移动得更远，当 Y 轴处于其行程的极限时，它快速摆动到位，当机架向后移动时，它缩回。另一个很好的补充是安装在一侧的工具深度传感器(又名:开关)，它允许机器找到每个工具的底部，如果它是未知的，那么 Z 轴可以补偿。当结合自动伸缩防尘鞋，这绝对是一个数控建设，我们希望看到在我们附近的商店！

这些年来，我们有相当多的 CNC 黑客，包括刀具更换器，[像这个](https://hackaday.com/tag/automatic-tool-changer/)，但是 [3D 打印机也可以使用一些刀具更换器爱](https://hackaday.com/2021/06/12/magnets-how-do-they-work-on-3d-printers/)！

 [https://www.youtube.com/embed/ZeOUdosoEBM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ZeOUdosoEBM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

