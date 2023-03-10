# 一种 GPS 频率标准，用于确定何时需要正确的时间

> 原文：<https://hackaday.com/2022/06/29/a-gps-frequency-standard-for-when-the-timing-has-to-be-right/>

计量极客将竭尽全力确保他们的测量是最好的，他们的仪器是最精确的，他们的校准是准确无误的。曾几何时，对于时间和频率爱好者来说，这是一项困难的工作，但随着头顶上携带超精确原子钟的 GPS 卫星的出现，准确无误的频率变得令人惊讶地容易。[Land-boards]有一个基于一组模块的 GPS 10 MHz 时钟。

由于许多 GPS 模块具有 10 MHz 输出，人们可能会认为这个模块只是简单地将一个插座连接到模块上，但它使用了他们的另一个项目，一个快速边沿脉冲发生器，将 GPS 输出作为振荡器，作为缓冲器和信号调节器。再加上一个 QT Py 微控制器板来设置 GPS，你就有了一个独立的 10 MHz 信号源，可以与任何标准相媲美。完整的细节可以在项目的 wiki 上找到，固件可以在 GitHub 上找到。

在探索标准频率时要小心，[因为这可能会导致兔子洞](https://hackaday.com/2018/01/17/confessions-of-a-reformed-frequency-standard-nut/)。