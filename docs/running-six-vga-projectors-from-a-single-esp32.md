# 从单个 ESP32 运行六个 VGA 投影仪

> 原文：<https://hackaday.com/2021/08/18/running-six-vga-projectors-from-a-single-esp32/>

今天的微控制器是高速的发电站，可以做绝对奇妙的事情。凭借快速的时钟速度和特殊的 DMA 硬件，通常有可能实现表面上看起来几乎荒谬的伟大壮举。[Bitluni]决定证明这一点。)来自单个 ESP32 的 VGA 显示。(视频，下面嵌入。)

ESP32 的最高时钟频率为 240 MHz。它还具有一些漂亮的 DMA 硬件和 GPIO 映射，这使它非常适合这项任务。[Bitluni]因此能够将其设置为以每像素一位的单色输出驱动多达六个 VGA 显示器。或者，将六个输出引脚分成两组，每组三个，他能够运行两个 3 位颜色的 VGA 显示器。在这两种情况下，分辨率都是令人印象深刻的 640 x 400，并且[Bitluni]通过驱动六个带有 starfield 显示器的投影仪来演示硬件。

有用吗？也许还没有，但我们肯定能想到一些应用。请在评论中分享你自己的想法。与此同时，请查看[Bitluni]为 ESP32 撰写的其他优秀作品。

 [https://www.youtube.com/embed/HEM04lS2R-Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/HEM04lS2R-Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



【感谢 anacierdem 的提示！]