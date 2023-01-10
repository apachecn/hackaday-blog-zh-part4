# 老式计算器的设计显示了我们今天是多么的理所当然

> 原文：<https://hackaday.com/2021/02/20/vintage-calculator-design-shows-just-how-much-we-take-for-granted-today/>

[阿门]70 年代的 Rockwell 920 计算器在当时是一个非常令人印象深刻的硬件。它有一个 16 位显示器，一台打印机，还能运行程序。它甚至有一个磁卡读写器，可以用来存储外部程序和数据。用今天的眼光来看，它不太像计算器，更像我们所说的单板计算机。它们也是进入另一个时代的窗口，在这个时代，我们认为理所当然的许多电气设计假设还没有发生。到了探究是什么让计算器运行的时候，[阿门]有很多工作要做，仅仅是让基本的工具运行起来。

例如，[amen]的 [Blue Pill](https://hackaday.com/2020/11/22/blue-pill-as-a-nerdy-swiss-army-knife/) (一种开源的多用途测试和测量工具)一方面是窥探内部工作的完美工具。然而，这些内部工作碰巧在-17 伏使用负逻辑，这意味着逻辑 0 是-17 伏，1 是 0 伏。哦，它使用一个奇怪的时钟速率，启动。既然蓝药丸不支持-17 V 负逻辑(有什么作用吗？)制作一个界面需要一些定制工作。一旦这种方法奏效，蓝色药丸就会被用于比赛。

不熟悉的元素并没有就此结束。例如，每个 IC 上的引脚采用交错布局，与我们大多数人(以及我们的工具、试验板和 IC 夹)所熟悉的 DIP 模式非常不同。至于处理器本身，[amen]可以访问 Rockwell 处理器和指令集的低级文档，但时序图令人费解，直到人们意识到处理器有两个不同频率的两个时钟输入，导致[amen]描述为四个独立的“时钟阶段”。

这些设计决策在当时肯定是有很好的理由的，它们甚至有一定的内在和谐，但它仍然是一个时代的窗口，当时支撑我们现在拥有和工作的许多元素还没有发生。

看看下面嵌入的视频，看看[阿门]解释是什么把蓝色药丸挂到了洛克威尔 920 上。此外，如果你想看看这些老式机器中的一个展示其所有功能的荣耀，[这里有一个视频正在测试它的速度](https://www.youtube.com/watch?v=mRxRr7Xm_wA)。

 [https://www.youtube.com/embed/I1Vrf0dEtaQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/I1Vrf0dEtaQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

