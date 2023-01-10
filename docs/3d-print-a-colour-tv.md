# 3D 打印彩色电视

> 原文：<https://hackaday.com/2022/05/27/3d-print-a-colour-tv/>

最古老的电视形式使用一个带有一系列孔的旋转圆盘——尼普可夫圆盘——将图像切割成线条进行显示。它们是令人惊讶的简单机器，尽管分辨率相对较低，但却能够拍摄出出乎意料的高质量图像。更好的是，在一个微控制器和明亮的发光二极管的时代，制造一个可以工作的不再是曾经的苦差事。[Markus Mierse] [已经创建了一个使用 Arduino Mega 和一组 3D 打印部件的电视，所以没有理由不在你的货架上放一个旋转的磁盘电视。](https://spectrum.ieee.org/mechanical-tv)

选择 Arduino Mega 是因为它有足够的线路来驱动三个 6 位 DAC，分别用于红色、绿色和蓝色。磁盘由 PWM 电机控制器驱动，同步由一块反光胶带和一个红外接近传感器负责。图像和视频从 SD 卡中读取，并以绚丽的 32 行彩色显示在屏幕上。完整的构建过程可以在下面的视频中看到。

当观看机械电视时，令人惊讶的是，它的质量比你所相信的低分辨率好得多，而且这台彩色显示器比通常的单色设备好得多。这几乎不是高清电视，但它表现得很好，会提供一个很好的话题。

如果你对尼普可夫圆盘感兴趣，[它们是我们过去研究过的课题](https://hackaday.com/2017/06/28/mechanical-image-acquisition-with-a-nipkow-disc/)。

 [https://www.youtube.com/embed/LmISP_fAAws?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/LmISP_fAAws?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

