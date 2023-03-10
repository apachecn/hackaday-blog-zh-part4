# 智能尺子有很多特点

> 原文：<https://hackaday.com/2021/12/02/smart-ruler-has-many-features/>

对于我们这些还记得老式球型鼠标的人来说，它们很像现代的光学鼠标，只是它们需要经常清洗。将光学鼠标作为与计算机交互的标准方式是对以前计算时代的重大改进。随着球形鼠标的灭绝，现在有不计其数的廉价光电鼠标，它们很容易被现代黑客攻击，来自[Vipul] [的这个最新项目展示了通过建立一个数字标尺](https://www.reddit.com/r/electronics/comments/r4zi4h/i_turned_an_old_mouse_into_this_detailed_video_in/?utm_source=share&utm_medium=web2x&context=3)来重新利用光电鼠标的一些方法。

从表面上看，构建似乎很简单。当尺子经过一个表面时，这个装置会精确地记录下它移动了多远，使它成为一个有效且非常精确的尺子。为了建造它，鼠标的光学组件被清除并通过 USB 直接与 Raspberry Pi Zero W 配对。最初他打算使用 ESP32，但无法使用 USB 接口。[Vipul]然后能够编写一些软件，可以直接从鼠标的 PCB 中读取信息，并将其转换为人类可读的形式，显示在小屏幕上。整个设备被安置在一个定制的 3D 打印外壳中，将所有东西包裹起来，但建造并没有就此停止。[Vipul]还利用了 Pi 的蓝牙功能，编写了一个智能手机应用程序，也可以用来控制尺子。

虽然该设备确实有一些限制，因为它必须与被测物体的整个长度接触，但在某些情况下，我们可以想象这样的东西非常有用，特别是在测量非直线的东西时。[Vipul]还公开了该项目的所有代码，供我们这些可能对此有其他用途的人使用。我们已经看到光学鼠标在过去被重新用于各种事情，包括测量自动驾驶汽车的行驶距离。

 [https://www.youtube.com/embed/3qj8BxbykvE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/3qj8BxbykvE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

