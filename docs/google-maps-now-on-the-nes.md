# 谷歌地图，现在在 NES

> 原文：<https://hackaday.com/2021/09/02/google-maps-now-on-the-nes/>

许多年前，谷歌创造了一个著名的愚人节玩笑，暗示它将为最初的任天堂娱乐系统制作 8 位版本的谷歌地图。[cicilusplus]决定它需要成为现实，但是，[并开始工作。](https://www.youtube.com/watch?v=5vcPnk-6saw)(视频，下面嵌入。)

这是一个合适的块状低分辨率实现，但它仍然是一个运行在 NES 上的地图应用程序。放大和缩小是通过 A 和 B 按钮，而 D-pad 是用来滚动。相关区域的国家和城市标签以迷人的老式字体呈现在地图上。

该项目使用 Raspberry Pi 3A+和 Cypress Semiconductor FX2LP 微控制器，该微控制器安装在 NES 墨盒内。它的工作方式与早期的 [NES 毁灭计划](https://hackaday.com/2019/06/06/doom-on-the-nes/)相同，后者使用树莓 Pi 向 NES 的图片处理单元提供数据。这是通过在墨盒内部的 ROM 上刻录一段简单的代码来实现的，这段代码启动 NES，并使其通过 FX2LP 从 Raspberry Pi 接收数据。

在目前的形式下，除了允许用户滚动和放大地图的一部分之外，它不能做更多的事情。然而，我们希望看到一个成熟的版本，可以提供驾驶方向或类似的功能。如果你最终实现了这样的壮举，一定要让我们知道。

 [https://www.youtube.com/embed/5vcPnk-6saw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/5vcPnk-6saw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

