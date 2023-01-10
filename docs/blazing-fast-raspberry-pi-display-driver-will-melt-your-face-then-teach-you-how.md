# 超快的 Raspberry Pi 显示驱动程序会融化你的脸，然后教你怎么做

> 原文：<https://hackaday.com/2018/10/21/blazing-fast-raspberry-pi-display-driver-will-melt-your-face-then-teach-you-how/>

读者[poipoi]最近写信给我们的提示行，告诉我们一个“惊人快速”的 Raspberry Pi 显示驱动程序和一个自述文件，“读起来是一种真正的快乐”。当然，我们必须自己去看。[由【juj】开发的 fbcp-ili9341 回购](https://github.com/juj/fbcp-ili9341)，似乎不负众望！软件本身给人印象深刻，自述文件详细，结构良好，有教育意义，我们敢说有娱乐性吗？

该驱动器的主要目标是通过 SPI 总线产生高达约 60 帧/秒的高帧速率，它可以在各种 Raspberry Pi 器件上运行，包括 2、3 和 Zero W，任何进入 Pi HDMI 端口的视频输出都将通过 SPI 总线镜像到 TFT 显示器。它可以与目前许多流行的显示器兼容，包括使用 ILI9341、ILI9340 和 HX8357D 芯片组的显示器。

README 的 [*如何工作*](https://github.com/juj/fbcp-ili9341#how-it-works) 部分详细解释了让[juj]从并不十分快速的串行总线中哄出这样的帧速率的技术，但很大程度上归结为这样一个事实，即它只为每帧发送*改变的*像素，而不是全屏。作者声称，当你玩像《雷神之锤》这样的游戏时，每次更新都会减少大约 50%的像素传输。还有其他有趣的性能调整，所以请务必查看回购协议以了解所有细节。

休息之后，有一个视频比较了 fbcp-ili9341 与主线 SPI 驱动器的性能。

 [https://www.youtube.com/embed/dqOLIHOjLq4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/dqOLIHOjLq4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



如果你想使用一个更轻量级的计算平台，我们已经为 [esp8266](https://hackaday.com/2017/04/08/everyone-loves-faster-esp8266-tft-libs/) 、 [esp32](https://hackaday.com/2017/07/03/esp32-display-is-worth-a-thousand-words/) 和 [teensy](https://hackaday.com/2014/08/18/tft-lcds-hit-warp-speed-with-teensy-3-1/) 介绍了类似的注重性能的 SPI 显示驱动程序。

[再次感谢提示 poipoi]