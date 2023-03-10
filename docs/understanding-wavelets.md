# 理解小波

> 原文：<https://hackaday.com/2022/09/10/understanding-wavelets/>

数学变换对理解信号很有帮助。试图观察复杂的波形并在没有傅立叶变换的情况下计算出频率成分的成像。[Artem Kirsanov]称[小波变换](https://www.youtube.com/watch?v=jnxqHcObNK4)为“数学显微镜”,他的视频对这个主题做了很好的介绍。你可以看下面的视频。

视频首先讨论了时域和频域如何具有双重关系，如果你已经处理过傅立叶变换，这不是什么大新闻，事实上，这是视频的下一个主题。然而，这种转换也有局限性，在转换过程中会丢失时域信息。

显然，小波变换可以解决这些限制。变换类似于应用傅立叶变换，但小波变换不是分解成一系列无限正弦波，而是将信号分解成满足特定条件的有限函数。

你确实需要一点数学知识来理解这个视频，但可能没有你想象的那么多。解释很清楚，对你先前的知识没有什么假设。如果你在傅立叶分析中遇到过窗口，想法有些相似。

如果你想在[电子表格](https://hackaday.com/2019/11/15/dsp-spreadsheet-iq-diagrams/)中试验一些 DSP 概念，你可以这样做。如果你没有直观地掌握傅立叶变换，可以试试看题目上的【3blue1brown 的】[启发视频](https://hackaday.com/2019/07/13/fourier-explained-3blue1brown-style/)。

 [https://www.youtube.com/embed/jnxqHcObNK4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/jnxqHcObNK4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

