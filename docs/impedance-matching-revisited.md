# 阻抗匹配再探

> 原文：<https://hackaday.com/2022/01/13/impedance-matching-revisited/>

如果你是射频设计的老手，你可能会很好地处理匹配阻抗。不过，如果你刚入门 RF，[【FesZ Electronic】关于无损阻抗匹配的最新视频系列](https://www.youtube.com/watch?v=-_T587mucaI)非常值得一看。

匹配很重要，原因有几个。当源阻抗和负载阻抗匹配时，功率传输最大。此外，在射频下，阻抗不匹配会导致反射，再次剥夺有用功率。视频讲述了一些数学知识，然后转到 LTSpice 来模拟测试电路。但是你真正等待的部分——实际电路——大约是 15 分钟。由于你需要的值经常是古怪的，[FesZ]自己制作了可调电感器，并使用微调电容器来调整实际电容值。

这是一个很大的话题，但第一个视频是一个很好的介绍，融合了理论、模拟和实践。这是入门基本 RF 设计技能的好方法。

如果你想再看一遍，我们已经在之前对[做了解释。如果你想了解为什么不匹配的阻抗](https://hackaday.com/2015/07/29/say-it-with-me-input-impedance/)[会导致更少的功率输出](https://hackaday.com/2016/02/29/spice-power/)，我们也已经做到了。

 [https://www.youtube.com/embed/-_T587mucaI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/-_T587mucaI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

