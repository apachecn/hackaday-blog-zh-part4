# 现代试管测试器使用 Arduino

> 原文：<https://hackaday.com/2021/09/24/modern-tube-tester-uses-arduino/>

曾经有一段时间，像我们这样的人可能拥有试管测试器，即使你没有，你也可能知道哪家药店有试管测试器可以免费使用。我们不确定这是对资本主义独创性的证明，还是对电子管可靠性的创造——也许两者都是。由于[天兔]一直在做一些基于管道的项目，他决定需要一个测试器，所以他[造了一个](https://www.youtube.com/watch?v=Yh8K46Id5sI)。你可以在下面的视频中看到结果。

测试人员仅使用 24V，但对于他正在构建的项目，这接近真实电路中的操作。他确实有一个传统的试管测试器，但它使用 100 伏的电压，这是一个不同的操作模式。

大部分电路正在产生所需的电压，包括一个 555 电荷泵来产生大约-10V 的电压。显像管以特定的配置连接，Arduino 在改变操作偏置条件时进行一些测量。转换器经过分压器，因此最大 24 伏不会使 Arduino 过载。

将数据抓取到电子表格中可以进行一些曲线跟踪，这对匹配很有用。然而，正如[天兔]所指出的，测试人员对自己的应用非常专一。他计划制造一种更通用的试管测试器。

真正通用的试管测试器的一个问题是连接到不同的引脚。穿孔卡片给出了一个答案。如果你不记得药店里的试管测试员，你可能会发现[电视维修](https://hackaday.com/2016/05/03/retrotechtacular-tv-troubleshooting/)，曾经是一笔大生意。

 [https://www.youtube.com/embed/Yh8K46Id5sI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Yh8K46Id5sI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

