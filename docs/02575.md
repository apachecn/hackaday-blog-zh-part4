# 一张照片和一些被动支持突破辉煌的 NTSC 颜色

> 原文：<https://hackaday.com/2019/03/29/a-pic-and-a-few-passives-support-breakout-in-glorious-ntsc-color/>

“从来没有两次相同的颜色”可能是一个恰当的贬义词，但在 20 世纪 50 年代支持模拟彩色电视而不放弃一个巨大的黑白接收器安装基础不是一个选项，最终国家电视标准系统委员会在他们被给予的限制内做了令人钦佩的工作。

由于需要妥协，NTSC 模拟信号不是最容易处理的，尤其是当你试图用微控制器产生它们的时候。这款基于 PIC 的突围式游戏设法用最少的外部组件轻松完成了任务。[Jacques]进行这一构建是为了向经典的*突破*街机游戏和驱动家庭版游戏的色彩标准致敬。除了 PIC12F1572 和晶体振荡器之外，只需要几个元件就可以产生色度和亮度信号以及水平和垂直同步信号。游戏本身是相当真实的，虽然从下面的游戏视频来看有点紧张和不可原谅。[Jacques]已经把所有的代码和原理图放到了[GitHub](https://github.com/picatout/breakout_1572)上，供那些希望恢复模拟辉煌时代的人使用。

觉得 NTSC 比 PAL 诡异？你说得对，这比你想象的还要奇怪。[【Matt】在 Stand Up Maths 上，我们不久前讨论过这个问题](https://hackaday.com/2016/10/06/never-twice-the-same-color-why-ntsc-is-so-weird/)，事实证明，29.97 fps 的帧速率实际上是合理的。

 [https://www.youtube.com/embed/vrqX9GyqXJU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/vrqX9GyqXJU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

