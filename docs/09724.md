# Arduino 为您的肖像设计风格

> 原文：<https://hackaday.com/2021/04/05/arduino-plots-your-portrait-with-style/>

在这些零件周围，我们看到大量绘图仪构建。这是一个学习数控机床的好方法，同时你也可以享受制作图片的乐趣。[Ben Lucy]正在进行这样一个他自己的构建，但是想要做一些独立的服务于一个目的的东西。结果是令人印象深刻的便携式肖像画家。

使[本]的项目与众不同的是它有多完整。不像其他绘图仪只是遵循 g 代码指令或处理外部图像，便携式肖像画家是一个完全独立的机器。它配备了一个 OV7670 相机，连接到一个 Arduino 上，能够拍摄自己的照片，然后也可以将它们画出来。

[通过来自【Indrek Luuk】](https://github.com/indrekluuk/LiveOV7670)的一些聪明的代码，Arduino Mega2560 能够在彩色 LCD 屏幕上显示 20fps 的视频预览。当用户按下按钮时，当前帧被捕获并发送到笔式绘图仪。绘图算法尤其令人印象深刻，图像首先经过直方图补偿处理，以最大限度地提高对比度。然后用笔在页面上逐行绘制，并根据每个像素的颜色值按不同的量压入页面。像素越暗，钢笔的笔画越粗。这种更具模拟性的方法产生的图像比更基本的绘图仪要详细得多，更基本的绘图仪要么留下标记，要么不留下。

绘图仪产生的人像令人印象深刻，我们喜欢页面边缘的工件，这为最终的结果添加了一点风格。这位肖像画家会成为任何创客大会或黑客空间之夜的热门话题。

这个项目让我们想起了这些年来我们见过的一些绘画机器人。休息后的视频。

 [https://www.youtube.com/embed/U5dt6qbI_Uw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/U5dt6qbI_Uw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

