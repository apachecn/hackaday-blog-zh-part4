# 在激光中寻找直线

> 原文：<https://hackaday.com/2018/08/04/finding-the-linear-in-a-laser/>

如果你曾经尝试过高保真音频，你会意识到失真对音质的影响。元件中最微小的非线性都会破坏结果，在高保真度频谱的极端工作的人会竭尽全力去追求人类可能听不到的最小百分比的失真。

[蒙他·埃尔金斯]有一个 Boldport 套件，Lite2Sound，顾名思义，它可以将光线水平转换为音频信号。如果给他一个激光二极管和一个来自亚马逊回声的乡村音乐源，也许他可以通过一束激光传输声音。考虑到 Lite2Sound 是一个全模拟设备，因此除非它包含一个低通滤波器，否则它可能会与 PWM 斗争，要实现这一壮举，他必须将乡村音乐直接调制到激光上。

在下面的视频中，他向我们展示了他如何通过在示波器上绘制其 VI 曲线来表征他的激光二极管，并确定其最线性的区域。然后，他能够在该区域的中间提供电压，并通过 RC 网络简单地覆盖来自回声的线路电平音频。结果是通过激光成功地传输了音乐，听起来不错，尽管我们会发现看看音频分析器会怎么做很有趣。我们也有兴趣知道 VI 曲线是否也映射到光强度中的相同轮廓，我们怀疑答案会是“足够接近”。

所以激光无线音频是可以实现的，任何人如果指出蓝牙也可以实现同样的壮举，那就扫兴了。毕竟，没有 [*该死的激光*](https://hackaday.com/2012/08/31/a-laser-audio-transmitter/) 什么是高保真！

 [https://www.youtube.com/embed/HiS1RX8Svzw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/HiS1RX8Svzw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

