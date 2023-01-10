# DIY 无人机的开源运动控制器

> 原文：<https://hackaday.com/2021/03/24/open-source-motion-controller-for-diy-drones/>

DJI 最近推出了一款光滑的运动控制器，它避开了传统的双杆发射器，让你只用一只手就能驾驶他们的新“FPV 无人机”。事实上，它看起来可以兼作 X 翼的控制杆，这只是一个额外的奖励。不幸的是，这款售价 199 美元的控制器目前只兼容这一款。不愿意被 DJI 的生态系统所束缚，[【帕韦·斯彼哈尔斯基】开发了一个开源的类似工作的运动控制器](https://github.com/DzikuVx/DiyMotionController)，为自制的四轴飞行器和飞机带来手势飞行。

现在要明确的是，你仍然需要一个传统的发射机来使用这个设备。Pawe 没有尝试重新发明轮子，而是决定将他的运动控制器作为 OpenTX 硬件(如 RadioMaster TX16S)的附加设备来实现。它只需插入发射机背面的训练器端口，作为辅助输入。这大大简化了设计，因为它基本上只需要从其 MPU-6050 陀螺仪/加速度计读取角度数据，并通过串行端口将其转发给 OpenTX。此外，它连接到训练器端口的事实意味着，如果出现任何问题，您可以立即禁用它并返回到传统控制。

除了运动感应装置，ESP32 驱动的外设还具有一个拇指棒和一对按钮，位于其 3D 打印框架中。一个有机发光二极管显示器提供一些用户反馈，一个 18650 电池的支架安装在背面，因为当[pawez]开始与发射器无线连接时，控制器将需要自己的电源。

在下面的视频中，[pawe]对运动控制器进行了测试飞行，并对结果非常满意。正如你对第一次尝试的预期，一些调整正在进行中，但没有什么会阻止你今天构建自己的版本，并体验可能是遥控飞行的下一次演变的[。](https://hackaday.com/2017/11/20/can-commodity-rc-controllers-stay-relevant/)

 [https://www.youtube.com/embed/1e1Dzy56vOk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/1e1Dzy56vOk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

