# 可爱的示波器使用发光二极管进行显示

> 原文：<https://hackaday.com/2022/03/29/cute-oscilloscope-uses-leds-for-display/>

示波器曾经通常被称为 cro，因为它们依靠阴极射线管进行显示。从那以后，技术发展很快，示波器现在几乎完全依赖于像液晶显示器这样的现代屏幕。然而，[lonesoulsurfer]通过这个有趣的 DIY 构建走了一条不同的路线，创建了一个带有低分辨率 LED 显示屏的示波器。

是的，信号显示在由红色发光二极管组成的 10×10 矩阵上。由于[lonesoulsurfer]能够为该建筑提供 5 毫米见方的 led，单个像素看起来扩散得很好，而且很厚实。整个项目仅使用四个 ICs 一个十进制计数器和一个运行显示器的 LM3914 LED 驱动器、一个用于时钟输入的 555 定时器和一个用于放大输入信号的 LM386 运算放大器。

通过板载麦克风，示波器可以充当简单的音乐可视化工具，或者与探针一起使用来研究实际电路。对于精细的工作来说，它可能没有足够大的分辨率或精度，但如果你对一个简单项目的功能感到困惑，它至少会告诉你微控制器的时钟是否正常运行。

这些年来，我们已经看到了一些很棒的 DIY 示波器，[比如这个整洁的基于 Arduino 的构建](https://hackaday.com/2018/09/21/building-a-pocket-sized-arduino-oscilloscope/)。休息后的视频。

 [https://www.youtube.com/embed/FqV2W9gObf8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/FqV2W9gObf8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

