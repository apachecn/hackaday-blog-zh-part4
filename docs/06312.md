# 伺服动力 7 段编排这款计时码表

> 原文：<https://hackaday.com/2020/04/22/servo-powered-7-segments-choreograph-this-chronograph/>

好钟通常是那些走时准确的钟。但是我们认为一座伟大的钟的标志是能够吸引观察者观看时间流逝。手表有多技术并不重要——看着沙子在沙漏中晃动也有它的好处。但就在我们确信 7 段钟领域没有什么新东西可做的时候，[【the diylife】说了句‘拿着我的啤酒’，并创造了这种美](http://www.instructables.com/id/Mechanical-Seven-Segment-Display-Clock/)。

总共有 28 个伺服系统用于独立控制四台显示器的 3D 打印部分。伺服系统将每个片段在两点之间来回旋转 90 度:向上和平面显示时间，然后在不需要时向下侧躺着休息。

就电路而言，这个时钟并不复杂，尽管它看起来确实很耗时。伺服系统由 Arduino 通过一对 16 通道伺服驱动器控制，分为 HH 和 MM 段。Arduino 从 DS1302 RTC 模块获取时间，并将结果分割成四位数的时间。就代码而言，每个数字都有自己的数组，其中存储了每个伺服系统的活动和非活动位置。演示和完整的构建和代码解释将在休息后等待。

说到 7 段显示器，我们说越多越好。这里有一个几乎使用了所有这些功能的时钟。

 [https://www.youtube.com/embed/SKNxyh06X1c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/SKNxyh06X1c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

