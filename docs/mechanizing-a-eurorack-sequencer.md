# Eurorack 测序仪的机械化

> 原文：<https://hackaday.com/2018/12/06/mechanizing-a-eurorack-sequencer/>

Eurorack 已经接管了合成器社区，数百人正在构建自己的 eurorack 模块。[Michael Forrest] [设计并制造了他自己的 Eurorack 序列器模块](https://www.youtube.com/watch?v=45-4xLrRMqg)，它不使用电容器和芯片等奇怪的东西来存储信号。相反，他用步进电机和一些巧妙的工程技术来做这件事。

Eurorack 序列器的基本思想是以某种方式存储一系列值，并重复播放它们。将这个序列与一个时钟相连，你就能从合成器中得到相同的声音模式。这可以用一个环形缓冲器以数字方式完成，在模拟域中用一堆 fet 和电容完成，或者在这种情况下，用一张纸粘在步进电机上。

这种结构的关键是一个步进电机，每转 96 步。这一点很重要，因为模块是由序列发生器的时钟脉冲控制的。因为 96 能被 8 和 16 整除，这意味着这个序列器将在 4/4 时间内播放。每分辨率 200 步的 NEMA 17 发动机在这种情况下根本不起作用。更确切地说，它在技术上是可行的，但将无法使用。

这种构建的电子设备出奇地简单，Arduino 接收时钟脉冲，并将步进信号发送给 H 驱动器。电机旋转一个纸盘，用光敏电阻和 LED 读取。它简单到有趣，是的，它被安装在一个适当的欧洲机架大小的面板上。你可以看看下面的视频。

 [https://www.youtube.com/embed/45-4xLrRMqg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/45-4xLrRMqg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

