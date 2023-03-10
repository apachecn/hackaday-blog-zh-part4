# 通过 Raspberry Pi Pico 实现 Z80 视频输出

> 原文：<https://hackaday.com/2021/11/28/z80-video-output-via-the-raspberry-pi-pico/>

从头开始构建基本的计算机是黑客社区中一种流行的消遣方式。[Kevin]就是这样一个爱好者，他决定为他的复古 Z80 机器设计一个视频界面。

![](img/78b97488c745b0426523de05a2d9f1ce.png)

输出来自【凯文】的构建。

涉案电脑为 RC 2014 Classic】[，[一款流行的单板 8 位电脑套件](https://hackaday.com/2016/09/08/review-the-rc2014-z80-computer/)。作为标准配置，它没有视频输出，所以[Kevin]使用 Raspberry Pi Pico 的 PIO 接口做了一个。

74 系列逻辑被用于处理地址选择，使 Pico 和 Z80 能够有效通信。Z80 中的等待状态用于避免两者通信时老式芯片跳闸。Pico 输出 160 x 120 分辨率的视频，每像素 8 位颜色，使用简单的电阻梯形 DAC 实现基本 VGA。

构建是熟悉 Pi Pico 和 Z80 本身编程的好方法。也就是说，如果 Pi Pico 以 125 MHz 的默认时钟速率运行，可能只需在 Pi Pico 上模拟 Z80 即可，从而使 RC2014 缓慢的 7.3728 MHz 主时钟黯然失色。

如果你一直在构建自己的复古图形硬件，请告诉我们。我们喜欢[这种东西](https://hackaday.com/2021/05/18/retro-isa-card-means-old-slow-computers-no-longer-need-old-heavy-monitors/)在这里！