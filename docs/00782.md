# 机器人在一条连续的线上蚀刻素描艺术

> 原文：<https://hackaday.com/2018/09/28/bot-makes-etch-a-sketch-art-in-one-continuous-line/>

1960 年以 2.99 美元(今天为 25.00 美元)的天价推出，蚀刻素描成为婴儿潮一代玩具盒的标准发行项目。尽管这个玩具看起来很迷人，但很难看出它为什么有持久力:年轻的手指很难转动旋钮，对角线和平滑的曲线需要音乐会钢琴家精细的运动控制，无论我们画了什么，只要轻轻一碰平板电脑就被抹去了。

为了纠正这些错误，[Sunny Balasubramanian]不仅将一幅蚀刻素描机动化，还在某种程度上赋予了它自己的思想。对于那些不熟悉这个玩具的人来说，它基本上是一个手动的 X-Y 绘图仪，它将触控笔拖过玻璃屏幕的下侧，刮掉附着在玻璃上的银粉，以制作深色线条。当然，用步进器替换旋钮很简单，但驱动它们才是关键。[Sunny]把他的连接到树莓 Pi 上，写了一些 Python 代码来驱动它们。Pi 还接受输入图像文件，并对其进行处理，以便通过绘图仪进行渲染，首先在 OpenCV 中进行 Canny 边缘检测，然后通过图像中最大的连接像素集合绘制一条路径。从那以后，只需旋转马达就能创造出令人惊讶的细节图像。看看下面的视频短片，看看它是如何工作的。

这并不是我们见过的第一个自动蚀刻草图的例子—[这里有一个自动蚀刻草图的例子](https://hackaday.com/2012/05/14/your-mug-on-an-etch-a-sketch-automatically/),包括摇动来擦除草图。不过这个有点作弊，因为它像 CRT 一样在屏幕上扫描。我们真的很喜欢这种单路径的方式。相当聪明。

 [https://www.youtube.com/embed/dieIlMUOwns?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/dieIlMUOwns?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

