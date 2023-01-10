# 你也可以建造大的 RGB LED 立方体

> 原文：<https://hackaday.com/2021/11/04/big-rgb-led-cube-you-can-build-too/>

LED 立方体真的不是什么新鲜事，我们许多人认为建造一个好尺寸的立方体几乎是电子产品的成年礼，没有那么多人设法找到时间或有能力实现它。我们很高兴[将您的注意力吸引到一个可爱的建筑上](https://www.youtube.com/watch?v=ciaFar8nfHc)，展示了所有涉及的过程、问题以及在此过程中找到的解决方案。

建造一个小立方体是一件微不足道的事情，尤其是在不考虑 PWM 颜色混合的情况下，然而简单的数学将会说明，随着你增加每一边的 led 数量，总数将会很快变得相当大。更多的 led 需要更多的功率，并大大增加了控制的复杂性。像这种 16 x 16 x 16 LED 构造的更大矩阵总共有 4096 个。这将是一个用普通 RGB LEDs 驱动的噩梦，即使是巧妙的多路复用，但幸运的是，你可以买到通孔封装的可转位 led，类似于你在周围看到的无处不在的基于 WS2812 的 SMT LEDs。这些都是基于 PD9823 控制器，可以像 WS2812 一样编程，至少根据[这个分析](https://cpldcpu.wordpress.com/2014/06/16/timing-of-ws2812-clones-pd9823/)。现在你可以简单地将一列发光二极管串联起来，控制信号从一个发光二极管传到最近的一个。

在视频构建日志的早期，您会注意到需要四个电源模块来提供这种能量。如果我们假设每个 LED 在全白模式下消耗 60 毫安(该产品链接的数据显示峰值为 100 毫安)，则总功耗仍为 246 安培，即约 1 千瓦。视频显示，整个阵列在全白的情况下，峰值功率测量值约为这个数字，因此数学计算似乎是正确的。

通过 Teensy 4.0 使用 IMXRT1060RM CPU 的 FlexIO 功能进行控制，如果需要，一组 74AHCT595 移位寄存器提供 32 个通道，每个通道最多 1000 个 led。粗略地说，使用带有 FlexIO 的 DMA，Teensy 每秒可以驱动多达 100 万个 LED 更新，这相当于大约 32 个通道，每个通道 100 个 LED 以 330 帧/秒的速度更新，因此有大量资源可用。所有这一切几乎都没有 CPU 的干预，腾出时间来处理基于 2.4 英寸 LCD 的用户界面和运行动画，如果你问我们，这看起来相当光滑。你可以在 [GitHub 项目](https://github.com/MaltWhiskey/Mega-Cube/tree/master/Documents/TriantaduoWS2811)的固件部分查看固件的描述。3D 打印夹具允许弯曲和夹住 LED 引线，以及固定和对齐 LED 柱单元，所以真的有足够的细节，让任何人都可以复制这一点，只要你能吞下所有这些 LED 的成本。

对于 LED 立方体的不同方法，请检查这种基于[甜蜜面板的方法](https://hackaday.com/2021/08/22/diy-led-cube-for-the-masses/)，这里有一个[非常小的 4x4x4 模块，适合那些空间较少的人](https://hackaday.com/2017/01/30/worlds-smallest-led-cube-again/)。

 [https://www.youtube.com/embed/ciaFar8nfHc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ciaFar8nfHc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



谢谢[基思]的提示！