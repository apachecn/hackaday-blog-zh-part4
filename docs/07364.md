# 优化微控制器的 GIF 回放

> 原文：<https://hackaday.com/2020/08/03/optimizing-gif-playback-for-microcontrollers/>

尽管早在 20 世纪 80 年代末就被 Compuserve 炮制出来了，gif 在现代互联网上又死灰复燃，主要是因为它们很有趣。然而，这些天我们所有的小型嵌入式系统都有了彩色屏幕，他们很乐意加入这个派对。[拉里·班克]为此想出了一个解决方案，让嵌入式系统用有限的资源播放简短的动画 gif。

[Larry]很好地解释了 GIF 格式是如何工作的，使用了 LZW 压缩和可变长度代码。他谈到了这种格式的设计是如何带来挑战的，尤其是在使用微控制器时。尽管如此，最终代码运行良好，能够处理大多数尺寸和结构合适的动画 gif。需要 24K 的 RAM，图像宽度限制为 320 像素。图像可以从闪存、内存或 SD 卡中加载，他指出，具有快速 SPI 的微控制器可以快速写入屏幕，从而获得最佳性能。

这是一个很棒的软件，承诺给微控制器项目增加许多魅力，或者愚蠢。它还简化了动画的使用，现在可以在计算机上设计，而不是使用板载图形库。GIF 确实是一种似乎永远不会消亡的格式；[在](https://hackaday.com/2016/10/23/the-animated-gif-camera-brought-to-you-by-a-raspberry-pi/)之前，我们已经展示了专用于表单的摄像机。休息后的视频。

 [https://www.youtube.com/embed/6GLCd0T9kB4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/6GLCd0T9kB4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/EUZGnyL_8xg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/EUZGnyL_8xg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

