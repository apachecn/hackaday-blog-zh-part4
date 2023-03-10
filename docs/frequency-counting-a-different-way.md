# 以不同的方式计数频率

> 原文：<https://hackaday.com/2019/09/12/frequency-counting-a-different-way/>

计算频率是表面上看起来简单的任务之一，但实际上有相当多的细微差别。有两种显而易见的方法，第一种是在一段时间内计算过零点。如果这个周期是一秒，你就完成了，否则这就是一个简单的数学问题。也就是说，如果你数了半秒，就把结果乘以 2，如果你数了 10 秒，就除以 10。另一个明显的方法是尽可能精确地测量单个周期的周期。然后就是这个[第三种方法](https://www.instructables.com/id/High-Resolution-Frequency-Counter/)。来自[WilkoL],它在测量频率的同时计算一个已知的参考时钟。你可以在下面的视频中看到结果。

第一种方法很简单，但是你想要测量的频率越低，你需要计算的时间就越长。此外，你需要准确的时间基准。对于第二种方法，您需要能够进行高度精确的测量。[WikolL]选择第三种方法的原因是它不需要非常精确的时基——一个中等精度的参考振荡器就可以了。该仪器在高频和低频下都能快速获得良好的分辨率。

进行测量的关键是一种连接 D 触发器的巧妙方法，它在固定的时间内对高频参考时钟和目标低频进行计数。固定周期不一定要很准。您最终得到两个计数:在此期间您看到了多少个输入时钟和多少个参考时钟。既然你知道参考时钟的频率，剩下的就是简单的数学运算了。

像这样的项目的真正危险是你可能很快沉迷于测量频率和时间。当然，我们已经见过很多[门控柜台设计](https://hackaday.com/2012/11/06/7400-frequency-counter/)。

 [https://www.youtube.com/embed/qTzbP1BKhmU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/qTzbP1BKhmU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

