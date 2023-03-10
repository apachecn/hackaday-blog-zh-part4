# 车道保持遥控汽车使用 OpenCV

> 原文：<https://hackaday.com/2019/10/16/lane-keeping-rc-car-uses-opencv/>

汽车制造商继续承诺完全自动驾驶汽车即将到来，但我们还没有完全实现。然而，近年来市场上出现了各种各样的驾驶员辅助技术，车道保持辅助就是其中之一。[【Raja _ 961】决定用树莓 Pi 在一辆 RC 车上实现这项技术。](https://www.instructables.com/id/Autonomous-Lane-Keeping-Car-Using-Raspberry-Pi-and/)

一辆常规的现成 RC 汽车被用作平台的基础，配备有两个驱动马达和用于转向的第三个马达。不幸的是，这辆车只能左转或右转，这限制了转向的技巧。尽管如此，工作仍在继续。一台 Raspberry Pi 3 配备了电机控制器和摄像头，并连接到底盘上。一切就绪后，使用 Python 脚本和 OpenCV 来运行车道保持算法。

[raja_961]很好地解释了车道保持方法。Instructable 分解了算法如何工作的每个阶段，而不是简单地调用一个库并称之为好的。在一系列操作用于挑选车道线的明显斜率之前，输入的图像被转换到 HSL 颜色系统。然后使用 PID 算法来指导汽车的转向。

这是一个基本车道保持算法的全面解释，如果你有兴趣了解这项技术，这是一个很好的起点。自动驾驶遥控汽车的世界里有很多正在发生的事情，你只需要知道去哪里找！休息后的视频。

 [https://www.youtube.com/embed/XqUFl8Azax4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/XqUFl8Azax4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/RJfrpWfj3_M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/RJfrpWfj3_M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

