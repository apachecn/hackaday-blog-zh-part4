# 低分辨率显卡仍然令人惊叹，因为它是由逻辑芯片制成的

> 原文：<https://hackaday.com/2019/07/07/low-res-video-card-is-still-amazing-since-its-made-out-of-logic-chips/>

[Ben Eater]已经在实验板上制作计算机有一段时间了，同时还做了一些教程和指南，如 YouTube 视频。一些有事业心的黑客已经复制了[Ben]的成果，但到目前为止，所有这些构建只是一堆发光二极管和开关。下一个前沿是视频卡，但它只能显示完全建立在试验板上的电路的数千个像素。

本文首先回顾了 VGA 标准，最终确定采用 800×600 分辨率、60 MHz 时序的显示器。该视频卡的像素时钟从 40 MHz 下降到 10 MHz，最终显示的分辨率将为 200×150。这足以显示图像，但首先[本]需要得到正确的水平时间。这意味着一个电路来计算像素，并在每条水平线的末端注入前沿、同步脉冲和后沿。

为了产生一条水平线，[Ben]的电路首先必须计数出 200 个像素，发送一个消隐间隔，然后将 sync 设置为低电平，最后是另一个消隐间隔，然后滚动到下一条线。这是通过一系列 74LS161 二进制计数器实现的，这些计数器设置为简单地从 0 计数到 264。为了产生前沿、同步和后沿，设置三个 8 输入与非门，在水平扫描线的相关点发送低信号。

整个构建占用了 4 个无焊试验板，使用了 20 个逻辑芯片，但这还没有完成:所有这些芯片和导线的虚构只是遍历水平和垂直行的像素数据。VGA 监视器检测到它处于正确的模式，但没有实际数据——这将是这个版本下一部分的重点，在这里[Ben]开始将像素推送到监视器。

 [https://www.youtube.com/embed/l7rce6IQDWs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/l7rce6IQDWs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

