# 大屏幕上的 GBA:FPGA 提供 HDMI 和所有可以想象的功能

> 原文：<https://hackaday.com/2018/12/02/gba-on-the-big-screen-fpga-delivers-hdmi-and-every-feature-imaginable/>

用家用游戏机创造便携式游戏的概念已经存在了一段时间，但很少看到其他方式。已经有一些设备敢于跨越界限(如世嘉游牧，任天堂 Switch 等。)，但这两个世界通常保持分离。[Stephen]试图通过将 Game Boy Advance 转变为“大男孩”控制台来探索这一领域。他创建的基于 FPGA 的 mod kit 就是这样做的，并通过迷你 HDMI 电缆提供控制器支持和 720p 数字视频输出。

该套件本身是专门为包含 40 针 LCD 带状电缆的原始型号 GBAs 设计的。这些最初的型号是早期运行的非背光屏幕，也由主板名称表示，可以通过窥视电池盒看到。通过移除手持设备的屏幕，使用新的扁平柔性带状电缆，可以直接从 GBA LCD 插座读取 RGB 信号。这种方法实现了无噪声的数字到数字解决方案，而不是任天堂自己的 Game Boy Player 插件 GameCube 的数字到模拟输出。

![](img/9f1763fba2fe200d4ffb15eb024a929e.png)

在惊人的 240×160 原生分辨率下，GBA 视频在 720p 帧内被 FPGA 放大了 5 倍。当然，一些图像在这个过程中被截断了，所以包括了 4x 和 4.5x 缩放的选项。正如一位智者曾经说过的，“不留下任何像素”。由于任天堂将 GBA 时钟设计为 59.7276 Hz，因此[Stephen]移除了振荡器晶体，以便将刷新率同步到更友好的 HDMI。这意味着 mod kit 稍微超频了 GBA 游戏，尽管[Stephen]包括了一个 GBA 循环精确模式作为选项，如果你的显示器可以处理它的话。

下面的视频是[Stephen]使用 SNES 控制器的初始测试。测试一定进行得很顺利，因为他决定在最终设计中加入 SNES 控制器端口。现在，由于这个“安慰者”套件，GBA 上的所有超级任天堂端口再次回到了家。

 [https://www.youtube.com/embed/8hb8VYtQU2E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/8hb8VYtQU2E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



对于那些寻求全面了解所有游戏男孩到电视视频解决方案的人来说，RetroRGB 也有一个很棒的视频可以观看。