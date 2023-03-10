# 身份错误—压电致动器不是测试垫

> 原文：<https://hackaday.com/2021/06/18/mistaken-identity-piezo-actuators-not-test-pads/>

EEVBlog 实验室的 NAS 中的一个硬盘最近出现了故障。忠于他的口头禅，[戴夫“撕开它”琼斯]打开它，给我们一个现代硬盘驱动器的内部参观。如今，现代硬盘中有如此多的技术奇迹——机械设计、电子和磁性，以及基本上是一种高级 RF 接收器的信号处理本身——我们可以原谅[Dave]掩盖压电执行器系统，认为它们是在制造测试点。即使知道它们是致动器，你也必须盯着它们，并在大脑接受它之前思考一会儿。

后来意识到这个错误，他制作了一个后续视频(下图),重点是磁盘磁头致动器臂和这个微致动系统(或者它们可能是微致动器)。基本概念是一对压电传感器，安装在支撑读取头的短臂的两侧。据推测，它们被异相驱动以向左或向右弯曲手臂，但这种运动是肉眼察觉不到的——即使在放大的情况下，[戴夫]也无法辨别他对传感器施加脉冲时的任何运动。当你考虑到这些微致动器安装在主致动器臂上，而主致动器臂本身也在运动时，保持纳米精度的嵌套控制环路安排确实令人惊叹。查看由 Western Digital 制作的这个 45 秒的解释性视频,其中有一个很好的概念动画。

![](img/d822a21145f3b77099fac950dc410079.png)

如果你想在不拆开硬盘的情况下看到它的运行，看看我们上个月写的透明硬盘。要阅读更多关于深奥的致动器的内容，请查看【2015 年的这篇文章，其中包含了我们页面上出现的最长的单词之一——*磁流变*。如果你经历过硬盘故障，谢天谢地，这种情况现在越来越少了，你会把它分成几块还是拆开？

 [https://www.youtube.com/embed/fUV8QQwCrh4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/fUV8QQwCrh4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

