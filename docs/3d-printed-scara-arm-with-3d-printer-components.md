# 带有 3D 打印机组件的 3D 打印 SCARA 手臂

> 原文：<https://hackaday.com/2020/10/08/3d-printed-scara-arm-with-3d-printer-components/>

3D 打印机兴起的一个副作用是 3D 打印机组件的可用性增加和成本降低，这些组件被用于各种应用。[How To Mechatronics]利用这一点，使用 3D 打印零件和普通的 3D 打印机组件建造了一个 [SCARA 机械臂](https://howtomechatronics.com/projects/scara-robot-how-to-build-your-own-arduino-based-robot/)。

基本的 SCARA 机构是一个双连杆臂，类似于人的手臂。通过在机构的基座和弯头处旋转，第二个关节的末端可以在 XY 平面中移动。[How To Mechatronics]通过用丝杠移动四个垂直线性杆上的第一个臂的基座，增加了 Z-motion。推力轴承和滚珠轴承的组合允许每个关节平稳旋转，关节由 NEMA17 步进电机驱动。每个关节在其旋转的某个位置都有一个微动开关，以给它一个初始位置。夹具的钳口在两个平行的线性杆上滑动，并由伺服系统驱动。为了控制电机，使用了 Arduino Uno 和 CNC 步进屏蔽。

该手臂由一台计算机操作，该计算机带有一个用 Processing 编写的 GUI，它通过串行向 Arduino 发送指令。GUI 允许关节的直接正向运动控制和反向运动控制，这将自动地将手爪移动到指定的坐标。GUI 还可以保存位置，然后将它们串在一起自动完成任务。

由于手臂其余部分的重量，底部关节有点摇晃，但这可以通过使用框架在顶部支撑来固定。我们非常喜欢使用常用的组件，第一段中的链接有详细的说明和源文件来构建自己的组件。如果剩余的间隙可以解决，它可能是一个体面的轻型数控平台，特别是与小足迹和大行程面积。这与我们之前见过的[木制 SCARA 机器人](https://hackaday.com/2019/03/14/wood-scara-arm-gets-a-grip/)非常相似，除了它把 Z 轴放在了手爪上。我们也看到了一些使用这种布局的 3D 打印机和[笔绘图仪](https://hackaday.com/2019/09/04/mechpen-scara-drawbot-for-the-big-picture/)。

 [https://www.youtube.com/embed/1QHJksTrk8s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/1QHJksTrk8s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

