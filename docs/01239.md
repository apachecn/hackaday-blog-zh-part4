# 超级任天堂的内存映射方法

> 原文：<https://hackaday.com/2018/11/14/memory-mapping-methods-in-the-super-nintendo/>

超级任天堂不仅是一个全方位的伟大平台，无论是在 20 世纪 90 年代的鼎盛时期还是现在的怀旧热潮中，而且与现代系统相比，它的相对简单性使它更容易从计算机科学的角度来看。这意味着我们可以对超级任天堂实际上是如何做的进行一些深入的讨论，并了解其中的大部分内容，就像这个来自[复古游戏力学解释]的视频，它对 SNES 的记忆系统力学进行了令人难以置信的详细描述。

SNES 使用的两个有趣的内存系统叫做 DMA 和 HDMA。DMA 代表直接内存访问，是超级任天堂独立于 CPU 访问内存的一种方式。这样做的好处是，与更典型的访问内存的方法相比，它的速度快得令人难以置信。这并不是特别独特，但 HDMA 系统是。它允许 SNES 用其视频输出显示做各种有趣的把戏，如改变颜色梯度和做各种遮罩效果。

如果你对像 SNES 这样的经典游戏机的内部工作方式感兴趣，这个视频会深入系统本身。有趣的是，程序员如何像 DMA 和 HDMA 系统那样操纵内存，从这些有限的(以现代标准来看)系统中挤出更多的能力。[复古游戏机制解释]是一个很好的资源，可以深入探索许多经典游戏，比如 speedrunners 如何在旧的马里奥游戏中执行任意代码。

 [https://www.youtube.com/embed/K7gWmdgXPgk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/K7gWmdgXPgk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

