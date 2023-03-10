# 电动相机支架曾经是一台 3D 打印机

> 原文：<https://hackaday.com/2022/08/17/motorized-camera-mount-was-once-a-3d-printer/>

如果你计划建造自己的电动相机支架，3D 打印机肯定会有所帮助。但在这种情况下，[dslrdiy]并没有用它来打印零件——他发现自己很少使用以前用废料建造的旧打印机，他决定重新利用它，将它变成一个能够平移、倾斜和滑动的[遥控 DSLR 相机支架](https://www.instructables.com/Turn-Your-Old-3dprinter-Into-a-REMOTE-4-AXIS-CAMER/)。

主要目标是不仅挽救步进电机和控制器板，在这种情况下，Arduino Mega 2560 与斜坡板，但也保持原来的固件本身在使用中。为了实现这一点，[dslrdiy]重新设计了机械部件，使他能够使用常规的 g 代码指令操作 X、Y 和 Z 轴来分别平移、倾斜和滑动，从而执行不同的相机移动。

g 代码指令本身通过 UART 由附带的控制盒发送，控制盒内装有 ESP32。这允许通过操纵杆和按钮或者通过串行蓝牙连接(例如从电话)来操作相机支架。ESP32 系统还允许设置预定义的移动位置，以及速度和其他电机调整。休息后，你可以在视频中看到所有演示。

虽然有更简单的相机安装解决方案，但这肯定是一个有趣的方法。它还显示了桌面 3D 打印机已经走了多远，如果我们已经发现老一代像这样重新利用。关于[dslrdiy]使用 3D 打印机和相机的更多作品，[查看他的可定制镜头盖](https://hackaday.com/2021/08/31/3d-printing-your-own-sturdy-lens-caps/)。

 [https://www.youtube.com/embed/CbL71S9tDSc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/CbL71S9tDSc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

