# 物体跟踪相机滑块获得良好的拍摄

> 原文：<https://hackaday.com/2019/11/24/object-tracking-camera-slider-gets-the-nice-shots/>

在这个时代，所有的休闲活动都必须在网上及时捕捉和货币化，相机滑块是热门商品。许多人从简单的手工构建开始，然后逐渐发展到更加灵活的机械化。[Saral Tayal]更进了一步，[实现了一个基本的跟踪模式，以拍摄更甜美的照片。](https://www.instructables.com/id/Object-Tracking-Camera-Slider-With-Rotational-Axis/)

该建筑的机械结构简单，依靠 8 毫米钢棒和线性轴承，这在 3D 打印机中更常见。一个 Arduino Uno 被压入服务运行显示，配备了有机发光二极管屏幕运行界面。RoboClaw 电机控制器用于控制所用的齿轮传动 DC 电机，一个控制直线运动，另一个控制摄像机的旋转。

随着编码器安装到电机上，RoboClaw 控制器使 Arduino 能够在滑块移动时跟踪滑块的位置和旋转。然后，可以给滑块一个对象相对于其自身的位置。通过一点数学计算，它将旋转摄像机来跟踪移动中的物体。

这是对典型滑块构造的简单添加，大大增加了可以实现的各种拍摄。也有很多方法来构建滑块，[就像我们在](https://hackaday.com/2018/12/27/motorize-your-camera-slider-the-hacker-way/)之前看到的那样。休息后的视频。


 [https://www.youtube.com/embed/s2miAggPVKs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/s2miAggPVKs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

