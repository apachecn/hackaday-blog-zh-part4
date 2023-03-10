# 简易频率计数器看起来不错，读数为 6.5 兆赫

> 原文：<https://hackaday.com/2020/12/10/easy-frequency-counter-looks-good-reads-to-6-5-mhz/>

我们被基于 Arduino 的频率计数器看起来有多吸引人所震惊。它也是一个相当简单的构建。它可以计数到 6.5 MHz，这不是很多，但即使有这种限制，也有很多事情可以做。

LED 显示屏无疑是复古的。在一个非常现代的 Arduino Nano 内部完成了大部分工作。有一个简单的整形电路来改善对不规则形状输入波形的响应。我们可能会使用单个运算放大器作为过零检测器。诚然，这有点复杂，但不会更复杂，它应该会给出更好的结果。

曾几何时，像这样的显示器意味着一些时间布线，但随着廉价的 Max 7219 板的出现，很容易将这样的显示器添加到几乎任何东西上。SPI 接口只需几根导线，所有的艰苦工作和布线都在模块上完成。

代码简短而甜蜜。由于 LED 驱动器和从 GitHub 借来的频率计数器组件，只有不到 30 行代码。

如果你增加一点硬件， [100 MHz 是一个容易的目标](https://hackaday.com/2016/09/09/very-simple-pc-frequency-counter-works-up-to-100mhz/)。常用的测量频率的方法至少有[三种。各有利弊。](https://hackaday.com/2019/09/12/frequency-counting-a-different-way/)

 [https://www.youtube.com/embed/pOKSlhwBEac?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/pOKSlhwBEac?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

