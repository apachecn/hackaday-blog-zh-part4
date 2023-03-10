# 用这款转向灯监控器让你自己更好地驾驶吧

> 原文：<https://hackaday.com/2021/11/07/annoy-yourself-into-better-driving-with-this-turn-signal-monitor/>

在任何给定的时刻，大约 99%的道路上的人会认为自己是一个高于平均水平的司机，这在统计学上是不可能的，因为它很容易被不经意的观察所否定。司机会犯各种各样的错误，但也许没有一种错误像不打转向灯那样恼人和可避免。[这个转向信号监控器](https://www.youtube.com/watch?v=dyKq7ub2Rco)旨在通过明智地使用负反馈来解决这个问题。

显然，[马克·拉迪诺维奇]觉得他有一种倾向，因为他开宝马，所以不打转向灯。为了打破这个让他失去第一辆宝马的习惯，他把 Arduino Nano 33 栓在方向盘和转向灯杆上。IMU 会感知每个人的位置，并通过蓝牙将其发送到 Arduino Uno WiFi。反过来，它通过 USB 与 Raspberry Pi 对话，Raspberry Pi 通过蓝牙连接到汽车的立体声系统，当方向盘转动但转向信号保持不变时，它会发出警报。下面的视频展示了它的使用情况；虽然它显然是有效的，但在很多情况下，即使没有真正要求打转向灯，它也会触发——例如，绕过环形交叉路口，或者在蜿蜒的道路上行驶到免下车窗口。

虽然[Mark]显然把这种舌头牢牢地扎在脸颊上，但我们不禁认为有更好的方法——嗅汽车的 CANbus 来确定转向角度和转向灯状态。如果你想要一个比[Mark]的解决方案更精简的解决方案，去年 Remoticon 上的这个关于 CANbus 嗅探的研讨会将是一个很好的起点。

 [https://www.youtube.com/embed/dyKq7ub2Rco?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/dyKq7ub2Rco?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[通过[汤姆的硬件](https://www.tomshardware.com/news/raspberry-pi-turn-signal-education-system)