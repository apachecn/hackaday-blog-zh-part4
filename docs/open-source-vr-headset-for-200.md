# 200 美元的开源虚拟现实耳机

> 原文：<https://hackaday.com/2020/09/13/open-source-vr-headset-for-200/>

我们以前见过自制的 VR 头戴设备，但是，它们通常依赖于特殊的软件，或者没有真正达到商业产品的水平。而来自[Max Coutte]和[Gabriel Combe]的开源项目 [Relativity](https://www.relativty.com) 则不然。[Max]说得好:

> 相对论不是消费品。我们在我的卧室里用烙铁和 3D 打印机制作了相对论，我们希望你也能这样做:自己制作。

与一些自制设备不同，相对论有完整的蒸汽 VR 支持。它还对基于视频输入跟踪身体的位置缩放提供了实验支持。

在外壳下，带有 Atmel ARM Cortex M3 和 IMU 的主板承担了繁重的工作，占 200 美元价格标签的 25 美元。固件可以在任何合适的 ArduinoCore 处理器上运行。显示器也有选项。你可以买 90 赫兹 1080 像素的屏幕，或者直接去 4K。原型使用 2K 双显示器，每秒 120 帧。

[![](img/042c421e35b6d657f0413624f8eca271.png)](https://hackaday.com/wp-content/uploads/2020/09/mb-3.png)

如果你想自己建立相对论，所有的细节都在 [GitHub](https://github.com/relativty/Relativty) 上，还有一个 [Discord](https://discord.gg/ByHFbtW) 服务器提供帮助。3D 打印的外壳看起来很棒，总体上看起来是一个令人印象深刻的设计。

我们已经看到[几个类似的项目](https://hackaday.com/2020/06/02/diying-a-vr-headset-for-cheap/)，有些甚至更便宜。我们实际上涵盖了来自同一个团队的耳机的[早期版本](https://hackaday.com/2018/01/22/we-couldnt-afford-an-oculus-so-we-built-one/)。你可以看到他们已经走了很长的路。