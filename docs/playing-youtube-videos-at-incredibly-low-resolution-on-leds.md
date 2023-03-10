# 在 led 上以极低的分辨率播放 Youtube 视频

> 原文：<https://hackaday.com/2021/03/10/playing-youtube-videos-at-incredibly-low-resolution-on-leds/>

自高清时代以来，数百万像素的屏幕已经变得司空见惯。分辨率已经飙升到平流层，媒体看起来从未如此清晰。然而，[gatoninja236]决定以另一种方式进行构建—[一种能够播放 Youtube 视频的 LED 矩阵。](https://www.hackster.io/gatoninja236/high-resolution-youtube-player-with-raspberry-pi-d6bdc9)

执行起来很简单。一个 Raspberry Pi 3，在一个 Python 脚本的帮助下，下载一个 Youtube 视频。然后，它通过 OpenCV 运行，OpenCV 解析视频帧，将其向下转换以适合 64×64 像素的显示。然后，只需将数据输出到连接到 Raspberry Pi IO 引脚的 64×64 RGB LED 矩阵，视频就可以在这里以低分辨率显示。

是不是特别有用的项目？不，这并不意味着它没有价值。它教授使用 LED 显示屏和从互联网上搜集的视频数据的有用技能。不过，如果你只是想要更多的像素，[这款乒乓电视墙可能更合你意](https://hackaday.com/2019/08/29/giant-led-display-is-1200-balls-to-the-wall/)。休息后的视频。

 [https://www.youtube.com/embed/VJywMjOct4g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/VJywMjOct4g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

