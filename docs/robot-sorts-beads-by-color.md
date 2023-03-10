# 机器人按颜色分类珠子

> 原文：<https://hackaday.com/2018/10/07/robot-sorts-beads-by-color/>

如果你认识做工艺品的人，他们大概有一个抽屉，里面有几百万颗散珠，混在一起。总有一天你会解决的，对吗？大概不会。当然，除非你造一个机器人来替你干脏活。这就是[Kalfalfa]所做的，使用一些 Phidgets 板、一个摄像头和 Open CV。你可以在下面看到纸板机做它的事情的视频。

也许这是因为我们更注重电子学，但我们对从漏斗中一次只抓取一颗珠子的机制印象深刻。如果你看录像，你就会明白我们的意思。然而，有时一个珠子卡住了，磁传感器会发现这一点，因此控制器可以反转一点，再试一次。

你会认为颜色检测会很难。曾经有一段时间，这将涉及过滤器和光传感器以及各种疯狂的旋转。现在只需要一个便宜的相机和 OpenCV。当然，RGB LEDs 也可以[去掉滤镜](https://hackaday.com/2017/08/29/color-sensor-from-an-rgb-led-and-a-photocell/)。

事实上，代码非常简单，所以如果你想尝试 Open CV，这可能是一个很好的学习方法，即使你不需要对珠子进行着色(是的，我们刚刚创造了这个词)。

奇怪的是，我们在[之前见过类似的机制，主要是用乐高](https://hackaday.com/2014/01/29/automatically-sorting-beads-by-color)制作的，但是——唉——2014 年的链接已经死了，尽管 YouTube 视频幸存了下来。

 [https://www.youtube.com/embed/Yb-lmpPeVw0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Yb-lmpPeVw0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

