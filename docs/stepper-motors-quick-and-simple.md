# 步进电机快速简单

> 原文：<https://hackaday.com/2021/04/09/stepper-motors-quick-and-simple/>

如果你想简单而容易地了解步进电机，可以看看[IMSAI Guy]的短片，其中他[设计了一个非常基本的步进电机控制器](https://www.youtube.com/watch?v=bZJoiB56N74)，并在此过程中加入了许多快速课程。(嵌在下面。)

他首先以实际动手的方式讲述了步进电机的基本原理，并向我们展示了如何在引脚未知的情况下完成连接。接下来，他演示了手动步进电机，然后制作了一个简单的 FET 驱动电路。就在你期待一个小型微控制器出现的时候,[IMSAI Guy]却在他的垃圾箱里翻箱倒柜，解释如何用 22V10 GAL(一种电可擦 PAL)和 555 定时器模块驱动电机。基于一个解释清楚的驱动线圈的逻辑表，一个引入卡诺图的巧妙方法，他继续用 WinCUPL 编写输出方程。

![](img/655dd4596c5100a7e5ff45dd2556edc9.png)

Mature Readers will recall the “Happy PAL” Character

WinCUPL 是 CUPL(通用可编程逻辑编译器)的现代版本，最初由一家名为 Assisted Technology 的公司编写，现归 Altium 所有。CUPL 和来自单片存储器公司(MMI)的 PALASM 和来自数据 I/O 公司的 ABEL 是专门为 pal、gal 和 CPLDs 设计的基本硬件描述语言。pal 是带有可熔互连的小型逻辑门阵列，你的设计被“烧”进熔丝中，就像(EE)PROM 一样。当与伙伴一起设计时，你可以清楚地在脑海中想象连接，现代 FPGAs 的出现弥补了这一点。

唉，他删掉了编译源代码和 22V10 编程的部分，直接跳到在试验板上测试电路。剧透警告——它确实有效。拉近镜头，眯着眼，他指出的漂亮的 555 定时器试验板模块被称为 TP353，你可以从你最喜欢的在线供应商那里找到。

在这个教程中有很多东西要学，并且[IMSAI Guy]在使这个主题对业余爱好者和新手变得平易近人方面做得很好。几周前，我们还讨论了他的另一个关于图像传感器的教程。感谢[itsevilbert]的提示。

 [https://www.youtube.com/embed/bZJoiB56N74?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/bZJoiB56N74?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

