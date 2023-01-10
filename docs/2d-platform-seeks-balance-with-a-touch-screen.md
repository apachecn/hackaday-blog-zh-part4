# 2D-平台用触摸屏寻求平衡

> 原文：<https://hackaday.com/2020/01/04/2d-platform-seeks-balance-with-a-touch-screen/>

这是一年中最令人兴奋的季节，这位康奈尔大学的教授提交了他的微控制器班学生整个学期都在做的项目。这些学生似乎并不缺乏想象力，每年的这个时候，我们总是期待着这些提示。

[Greg]和[Sam]的[触摸屏二维球平衡器](http://people.ece.cornell.edu/land/courses/ece4760/FinalProjects/f2019/ghk48_sof23/ghk48_sof23/ghk48_sof23/index.html)是[Land]学生成果的一个很好的例子。电阻式触摸屏由 3D 打印的万向平台支撑，并通过 hobby servos 在两个轴上倾斜。[Greg]和[Sam]选择使用 PIC32 上的 ADC 直接读取触摸屏的电压输出，以 2 kHz 在两个轴之间切换。实现了两个 PID 控制循环，以使球尽可能地位于平台的中心，下面的视频显示仍然有一些循环调整要做。但是考虑到业余爱好伺服系统的位置不精确和万向节的顺从性，我们对他们能够完全控制系统印象深刻。

当然，我们以前见过平衡球，但他们中的大多数都使用[摄像机](https://hackaday.com/2019/02/02/high-style-ball-balancing-platform/)或[麦克风](https://hackaday.com/2018/07/25/juggling-machine-listens-to-the-bounce-to-keep-ball-in-the-air/)来完成闭环。像这样在平台上看到直接感应是一个不错的改变。

 [https://www.youtube.com/embed/rfGH3TfaF4s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/rfGH3TfaF4s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

