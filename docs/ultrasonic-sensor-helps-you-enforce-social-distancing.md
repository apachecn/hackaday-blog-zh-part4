# 超声波传感器帮助你加强社交距离

> 原文：<https://hackaday.com/2020/04/09/ultrasonic-sensor-helps-you-enforce-social-distancing/>

如果你要出门(我们希望只是去基本的杂货店),而且你很难用眼睛测量出和其他人相距 6 英尺的距离，那么[圭多·博内利]可以为你提供一个解决方案。他用一个标准的旧 HC-SR04 超声波传感器、一个音频模块和一个驱动定制量针的伺服系统制作了一个设备[，如果你周围的人靠得太近而不舒服，这个设备可以警告他们](https://www.drduino.com/blogs/news/social-distance-arduino-project)。

虽然这个项目听起来很简单，但对于那些拥有一堆 Arduino 兼容的小模块，并且可能在业余时间制作过类似的东西的人来说，有一个关键组件给了它额外的润色。[Guido]发现超声波传感器的可靠性时断时续，并想出了一种巧妙的方法来平滑其输出，以便从中获得更准确的读数，使用了一种扭曲的气泡排序算法。从传感器收集 13 个数据点，然后对它们进行排序，以找到时间中点，位于该排序中心的三个数据点被平均为最终输出。也许不一定有科学的准确性，但正是我们所期望的解决这些问题的方法！

像这些帮助我们实施减缓病毒传播的措施的项目，可能是让我们忙于在实验室里修补的一个好赌注，就像[这些帮助你记住不要触摸你的脸的太阳镜](https://hackaday.com/2020/03/09/a-reminder-not-to-touch-your-face/)。请务必在休息后看看这一个！

 [https://www.youtube.com/embed/ItK8bS9YgVM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ItK8bS9YgVM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

