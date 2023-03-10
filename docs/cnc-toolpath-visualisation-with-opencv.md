# 使用 OpenCV 实现 CNC 刀具路径可视化

> 原文：<https://hackaday.com/2022/03/31/cnc-toolpath-visualisation-with-opencv/>

[Tony Liechty]在进入数控加工领域时遇到了一些问题——从简单的刳刨机开始，他被初学者常见的问题绊倒了，比如设计与工件形状的对齐、轴裁剪和工件/夹具碰撞。他做了像样的黑客的事情，并转向其他一些技术来帮助解决问题，并想出了一个相当简洁的方法来使用机器视觉和 OpenCV 来帮助[根据工件的图像现场预览刀具路径](https://www.youtube.com/watch?v=Ghqjpu9la84)(视频，嵌入在下面。)

ChArUco(棋盘和 ArUco 标记图案的组合)板贴在机器轨道上，用于为 OpenCV 提供空间点相对于图案场的位置参考，从而能够识别轨道图像中的像素位置。然后使用单应变换将两个侧面参考链接到工件的图像。此转换允许系统从工件图像中确定任何像素的物理位置，然后可以用所需刀具路径的图像覆盖它。然后，来自用户的反馈将使得能够实现路径的调整，例如移位或旋转，以便应对可以看到的任何问题。减少“愚蠢的”夹紧、定位和其他此类问题，意味着浪费的时间更少，废料箱中的材料更少，这只能是一件好事。

[Tony]说这个代码和设置只是概念的演示，但是这样“粗糙”的代码很可能是一些伟大事物的开始，我们将会看到。如果你想在家一起玩，就来看看 realworldgcodesinderster GitHub 吧！

我们已经看到了 OpenCV 在协助 CNC 应用方面的一些用途，比如这个很酷的[你画它，我来砍它，](https://hackaday.com/2022/03/24/you-draw-it-cnc-cuts-it/)以及这个使用机器视觉在 CNC 铣床上对一个大孔的中心进行[调零的方法](https://hackaday.com/2016/12/15/zeroing-cnc-mills-with-opencv/)。

 [https://www.youtube.com/embed/Ghqjpu9la84?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Ghqjpu9la84?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

