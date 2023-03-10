# 3D 打印飞行控制使用磁铁增强飞行模拟器 2020 体验

> 原文：<https://hackaday.com/2020/09/03/3d-printed-flight-controls-use-magnets-for-enhanced-flight-simulator-2020-experience/>

[![](img/1241643a3d2f744e9be8a50b69e5f67a.png)](https://hackaday.com/wp-content/uploads/2020/08/DIY-Hall-effect-controllers.png) 我们已经看到了不少使用霍尔效应传感器的 DIY 操纵杆设计，但[【Akaki Kuumeri】的控制器设计](https://www.youtube.com/watch?v=na3NeZJYK3g) (YouTube 视频，嵌入下文)真正充分利用了 3D 打印，避免了任何其他类型的制造。他一直忙于使用它们来增强他的微软飞行模拟器 2020 体验，并不仅分享了[他的操纵杆设计](https://www.thingiverse.com/thing:4576634)，还将它与[油门](https://www.thingiverse.com/thing:4578169)和[踏板](https://www.thingiverse.com/thing:4578174)的设计合二为一。

霍尔效应传感器输出与磁场成比例变化的电压，磁场通常由附近的磁铁提供。通过安装传感器和磁铁，使它们之间的距离根据控制器的移动方式而变化，可以检测位置并将其传送给主机。

在[Akaki]的案例中，这种通信是通过 Arduino Pro Micro(带有 ATmega32U4)完成的，其内置的 USB 支持允许其被配置和识别为 USB 输入设备。剩下的只是调整物理布局和获得正确的弹簧或弹性张力。你可以在下面的视频中看到这一切。

 [https://www.youtube.com/embed/na3NeZJYK3g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/na3NeZJYK3g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



霍尔效应传感器[在 DIY 操纵杆构建](https://hackaday.com/2018/01/18/flying-the-friendly-skies-with-a-hall-effect-joystick/)中具有特色，但要获得与众不同的令人愉快的东西，不要错过基于它们的[这个奇妙的高速磁成像仪](https://hackaday.com/2018/02/15/high-speed-imaging-of-magnetic-fields/)。