# LED 矩阵驱动指南

> 原文：<https://hackaday.com/2018/11/27/a-guide-for-driving-led-matrices/>

构建 LED 矩阵是一个有趣的项目，但也可能有点痛苦。通常是从手工焊接单个 led 和电阻开始，然后将它们连接到行和列，这样它们就可以由某种微控制器驱动。这是一项非常繁琐的工作，但您可以订购一个预先构建的 LED 矩阵，以节省一些时间和麻烦。尽管你仍然需要一个驱动程序，尽管你自己构建一个驱动程序是值得的，但是在进行这个项目的时候也有很多陷阱和权衡要考虑。或者，你可以将[视为【deshipu】已经详细概述的](https://hackaday.io/page/5596-driving-led-matrices-conveniently)中的若干驱动因素之一。

围绕驱动板的难题通常围绕着从 led 获得恒定亮度的问题，而不管一行或一列中有多少个同时被点亮。由于它们通常一次被驱动一行或一列，开得越多，每个 LED 的亮度越低。驱动板采用不同的方法来解决这一问题，通常包括高速扫描矩阵或使用恒流源，以消除对电阻的需求。[deshipu]概述了实现这些目的的四种流行芯片，他强调了它们的优缺点，以帮助任何希望建立类似东西的人。

这些电路板中的大多数都能让你轻松实现 8×8 的 LED 矩阵，也有一些在两个方向上高出几个像素。这可能足以满足我们的大部分需求，但对于更大的需求，您将需要其他解决方案，如本 [64×32 LED 矩阵时钟](https://hackaday.com/2018/07/10/morphing-digital-clock-will-show-you-a-good-time/)中的解决方案。如果[你进入额外维度](https://hackaday.com/2016/05/22/real-time-driving-of-rgb-led-cube-using-unity3d/)，还有更复杂的驱动因素。

图片来源:Komatta[公共领域]，来自[维基共享资源](https://upload.wikimedia.org/wikipedia/commons/thumb/b/b1/LED_RGB_matrix.jpg/512px-LED_RGB_matrix.jpg)