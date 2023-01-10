# 一种全自动电动碎罐机

> 原文：<https://hackaday.com/2019/01/13/a-fully-automatic-electric-can-crusher/>

我们这些回收空饮料罐的人知道这些容器带来的恼人的储存问题。对于一个只有很少金属的物体来说，一个罐头会占据很大的空间，如果你有超过平均水平的渴望，你很快就会被成堆的罐头占据很大的空间。解决方案当然是压碎它们，虽然有许多简单的解决方案涉及铰接木块或杠杆系统，但这是 *2019* ！我们有*机器*给我们那种东西！[万物机电]反正是这么认为的，因为他创造了[一台自动碎罐机，看着它是一种享受。](https://www.youtube.com/watch?v=ECL7-pYDClg)

它的核心是一个 120 伏交流电驱动的线性致动器，它可以压碎一个装在焊接钢导轨中的罐子。当罐头被压碎时，它会落入一个等待箱中，当致动器缩回时，一个新的罐头会从料斗中落下。控制由 Raspberry Pi 处理，有用于致动器的终端传感器和用于罐头料斗的光学传感器。目前的情况是，一旦最后一个罐子到位，机器就会停止，因为光学传感器记录料斗中没有罐子，但毫无疑问，软件更改可能会导致它在检测到最后一个罐子后执行一次压碎循环。

这台机器将是一个简单的工业自动化系统的理想候选者，但是无论它是如何被控制的，它都将把它的主人从令人尴尬的力量测试中拯救出来。看一看，我们已经发布了两个视频显示它在休息下的行动。

感谢[Baldpower]的提示。

 [https://www.youtube.com/embed/ECL7-pYDClg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ECL7-pYDClg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/HL0n6NQjSx4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/HL0n6NQjSx4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

