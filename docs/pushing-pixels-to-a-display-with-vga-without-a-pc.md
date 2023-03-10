# 在没有 PC 的情况下，将像素推送到具有 VGA 的显示器

> 原文：<https://hackaday.com/2019/07/17/pushing-pixels-to-a-display-with-vga-without-a-pc/>

[Ben Eater]回到了他的视频系列的第二部分，构建一个简单的视频卡，可以将 200×600 像素输出到显示器，只需要一个 VGA 连接，几个 74 逻辑芯片和一个 10 MHz 晶体。在本期节目中，我们将看到他如何只用一个电可擦可编程只读存储器和几个电阻将图像显示在屏幕上。

有趣的是，图像数据是如何编码到 EEPROM 中的，因为它必须与用于水平和垂直时序的电路相同。通过选择构成有效地址的相关输入，并将每个像素的大小加倍几次，可以将 100 x 75 像素的图像编码到 EEPROM 中，并使用该时序电路直接寻址。

EEPROM 本身的输出不直接馈入监视器，因为 VGA 接口期望每个 RGB 引脚上有一个 0 V 至 0.7 V 的信号来指示亮度。为了从这种设置中获得三种以上的颜色，[Ben]构建了一个简单的 2 位 DAC，允许每个通道两个位，这意味着每个颜色通道有四个亮度级别，即有效的 64 种颜色。

详情请见链接后的视频。虽然非常接近完美，但最后仍有一个小问题，即黑色竖线。这些是由电路中的定时问题引起的，YouTube 视频上的评论提出了各种其他潜在的修复方法。在[Ben]的下一个视频出来之前，你有没有试验过你自己的版本来调试这个问题？

 [https://www.youtube.com/embed/uqY3FMuMuRo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/uqY3FMuMuRo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

