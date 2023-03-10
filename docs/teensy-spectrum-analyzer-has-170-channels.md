# Teensy 频谱分析仪有 170 个频道

> 原文：<https://hackaday.com/2022/06/21/teensy-spectrum-analyzer-has-170-channels/>

虽然高保真音频在过去几十年中取得了长足的进步，但许多现代立体声设备仍然错过了一些老式模拟仪表，这些仪表在 60 年代至 80 年代的放大器和接收器中很常见。像 VU 米这样的东西不再常见，但在一些微控制器的帮助下，可以将它们重新构建到您的音响系统中。[Mark]向我们展示了如何利用[这款双音频可视化显示器](https://www.youtube.com/watch?v=DHQmH5JxDhE)恢复一些老派功能。

这种构建不仅包括两个显示器，而且微控制器实时跟踪 170 个通道以驱动显示器。更令人印象深刻的是，这一切都是在一个小小的 4.1 上完成的。为了帮助管理所有数据并保持尽可能快的速度，它使用焊接到板上的外部 RAM，第二个 Teensy 音频板用于进行实时 [FFT](https://en.wikipedia.org/wiki/Fast_Fourier_transform) 分析。大多数通道被发送到托管频谱分析仪的显示器，但两个通道被保留用于第二个显示器上的左右立体声 VU 计。

来自[Mark]的项目最初是基于[DIYLAB] 的这个软件，所以一切都是开源的。虽然它最初是为特定的硬件而构建的，但[Mark]设置了线路输入和线路输出以及麦克风输入，因此它现在几乎可以用于任何音频硬件。对于另一个经典的 VU 米，t [看看这个基于阿鲁迪诺](https://hackaday.com/2021/11/08/visualizing-audio-with-an-lcd-vu-meter/)的设计。

 [https://www.youtube.com/embed/DHQmH5JxDhE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/DHQmH5JxDhE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

