# 生活游戏中的电脑

> 原文：<https://hackaday.com/2020/11/21/a-computer-in-the-game-of-life/>

我们经常听到“图灵完备”这个术语，却没有过多考虑它的含义。从技术上来说，微软的 PowerPoint、Portal 2 和 Magic:聚会都是图灵完成的，那又怎么样呢？然而，每当有人开始一项令人难以置信的坚持不懈的探索，并用这些媒介中的一种创造出一台计算机时，我们都会敬畏地退后一步。

[Nicolas Loizeau]就是这样一个人，他在康威的《生命游戏》中创造了一台计算机。与电不同，生命的游戏使用滑翔机作为信号。因为两个正交的滑翔器可以互相抵消，或者形成一个滑翔器，如果它们以良好的相移相交的话，基本的逻辑门可以从这些相互作用中形成。这意味着门之间的空间至关重要，因为信号需要相位对齐。基本构件是一门 60 年代的枪，一个 90 度滑翔机反射器，一个滑翔机复制器和一个滑翔机吞噬者。

生成这些结构的所有 Python [代码都在 GitHub](https://github.com/nicolasloizeau/gol-computer) 上，因为机器的庞大规模不可能手工放置。Python 包含了将基本程序组装成一组可选滑翔机生成器的脚本。这一切都是基于 Golly，这是一个很好的模拟康威的生活游戏的程序，以及其他东西。虽然这不是生命游戏中的第一台计算机，因为[【保罗·伦德尔】在 2000 年发表了设计](http://rendell-attic.org/gol/tm.htm)，而[【亚当·古彻】在 2009 年发表了斯巴达通用计算机构造器](https://www.conwaylife.com/w/index.php?title=Spartan_universal_computer-constructor&oldid=8792)，我们认为这是一台特别漂亮的计算机。

实际架构有一条 8 位数据总线、一个带两个读取端口的 64 字节存储器、一个每行 21 位的 ROM 和一个支持 8 种不同操作的一键编码 ALU。指令有一个 4 位操作码，在几个不同的指令中解码。时钟是四个环，由滑翔机反射器随着滑翔机横梁的旋转而形成。这给了计算机四个阶段:执行、写入、递增 PC 和将 PC 写入内存。

生命的游戏是细胞自动机(CA)的一个很好的例子。还有其他几种类型的 CA，它们背后的历史非常有趣。我们之前已经讨论过这个领域，并深入研究了这个计算机科学的美丽边缘。看看下面的视频，真正感受一下[Nicolas]设计的机器的规模。

 [https://www.youtube.com/embed/8unMqSp0bFY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/8unMqSp0bFY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

