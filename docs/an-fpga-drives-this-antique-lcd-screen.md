# 一个 FPGA 驱动这个古董液晶显示屏

> 原文：<https://hackaday.com/2019/03/20/an-fpga-drives-this-antique-lcd-screen/>

如果你在台式机或笔记本电脑上阅读这篇文章，你可能正盯着 TFT LCD 显示屏上的数百万像素。TFT 因其图像质量和快速响应时间而成为主导技术，但它不是制造 LCD 的唯一方法。有更便宜的技术，如 STN 和它的颜色变体，CSTN。如今它们已经很少被使用了，但是[张文婷]有一辆放在附近，想试着开一开。

![](img/92e7f3fb2694743aeebae1a04d9fc60a.png)

Still scenes aren’t bad, but motion blur is readily apparent on any moving content.

有问题的屏幕来自一台 20 世纪的笔记本电脑。[是日立 SX21V001-Z4，](https://www.zephray.me/api/media/1535734517689-sx21v001-z4.pdf)分辨率 640×480 像素。CSTN 屏幕的驱动板曾经很容易得到，但是现在这样的东西很难得到。

[文婷]取而代之的是抓起 FPGA 开始工作。对于小型微控制器来说，驱动显示器可能是一项繁重的工作，因此在从事此类项目时，FPGA 始终是一个不错的选择。它们很容易产生任何需要的古怪信号，并且可以毫不费力地并行产生许多这样的信号。

[文婷]成功地让屏幕启动并运行，并连接到 VGA 输入。令人惊讶的是，静态图像的图像质量还过得去，尽管当引入运动时，事情绝对会变得一团糟。[【文婷】的演示展示了屏幕播放的《荒野之息](https://www.youtube.com/watch?v=hsehw-7-VTM)，它很好地展示了自 90 年代中期以来科技的进步。

驾驶奇怪的液晶显示器是黑客的成年礼，我们看到围绕这些部分的大量努力。休息后的视频。

 [https://www.youtube.com/embed/hsehw-7-VTM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/hsehw-7-VTM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

