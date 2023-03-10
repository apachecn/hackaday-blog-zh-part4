# 令人难以置信的慢电影，现在以耀眼的色彩播放

> 原文：<https://hackaday.com/2021/08/12/incredibly-slow-films-now-playing-in-dazzling-color/>

早在 2018 年，我们就报道过一个项目，该项目将视频分解成单独的帧，并在电子纸屏幕上缓慢循环播放。大约每三分钟就有一张新的图像推出，要“观看”一部正片需要几千个小时。当然，这不是重点。这个想法是把你最喜欢的电影变成一个艺术话题；一幅不断变化的肖像，你可以挂在墙上。

[【Manuel Tosone】最近受到启发，制作了他自己版本的这个概念](https://hackaday.io/project/177197-the-slowest-video-player-with-7-colors)，现在多亏了几年的电子纸开发，他甚至可以用彩色来制作。作为一个完美主义者，他决定用定制的 STM32 板驱动七色 5.65 英寸 Waveshare 面板，他估计六节标准 AA 电池可以运行近 300 天，并将所有东西包装在一个非常专业的 3D 打印外壳中。最终的结果是一个独一无二的*视频帧*，任何黑客都会自豪地展示在他们的斗篷上。

[![](img/39d9d01e0710246b6a9294081aa307b8.png)](https://hackaday.com/wp-content/uploads/2021/08/colorvidframe_detail.jpg) 黑客时代。该项目的 IO 页面包含精心策划的信息集合，涵盖从用于将视频文件处理到充满裁剪和增强图像的目录中的`ffmpeg`命令，到闪存寿命估计和能耗分析的所有内容。如果你曾经考虑过设置一个需要长时间运行的电子纸显示器，不管屏幕上实际显示的是什么，你很可能会在[Manuel]提供的精彩文档中找到一些有用的信息。

我们总是喜欢听到人们被他们在 hack aday 上看到的项目所激励，尤其是当我们把事情兜了一圈并展示他们自己对这个想法的看法时。谁知道呢，也许美化这些页面的下一个版本的电子纸视频框架会是你自己的。

 [https://www.youtube.com/embed/qn_BZIQWLiI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/qn_BZIQWLiI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

