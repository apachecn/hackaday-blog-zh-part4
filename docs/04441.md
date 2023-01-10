# 快速视频覆盖同轴电缆速度因子

> 原文：<https://hackaday.com/2019/10/11/fast-video-covers-coax-velocity-factor/>

我们曾经看到一个 C 程序员的面试测试，它展示了一个带有几个整数、浮点和指针字段的结构。问题是:这个结构有多大？正确答案要么是“视情况而定”，要么是“sizeof(struct x)”。“光速是多少？”这个问题也可以这么说。答案是每秒 186，282 英里，即每秒 299，792，458 米。然而，一个更好的答案是“这取决于它是什么旅行。”[KB9VBR]讨论了[不同的传输线如何具有不同的速度系数](https://www.youtube.com/watch?v=SCF15sDD2IM)，以及在进行 RF 测量时这意味着什么。速度系数为 0.6 的电缆可以看到无线电信号以 186，282 个数字的 60%移动。

这可能看起来像是卖弄学问，但是速度因子确实有所不同，因为它改变了诸如偶极腿和同轴短截线等东西的实际测量。这些人用信号发生器和示波器制作了一个临时的时域反射仪。

通过使用比英里/秒更容易管理的英制单位，他们计算出光速也是 11.78 英寸/纳秒。利用这些数字和它们的作用范围，他们可以利用脉冲传播的时间来比较电缆的长度和测量值。25 英尺的同轴电缆读作 24.96 英尺。一个商业仪器显示 24.87 英尺。非常好。时域反射仪也能发现同轴电缆中的问题，并告诉你问题出在哪里。

请记住，这些人是业余无线电操作员，可能不是物理学家。举个例子，当他随口说电子和亚原子粒子以光速传播时，你可能想核实一下。然而，从广播的角度来看，他们知道自己在说什么。声明一下，我们也不是物理学家，但是我们非常确定任何有质量的东西，比如电子，都不可能达到光速。

顺便说一下，构建良好的时域反射计的关键在于信号注入的快速上升时间。随着时间的推移，我们已经看到了相当多的[设计](https://hackaday.com/2015/07/27/hackers-measure-cable-lengths-with-time-domain-reflectometers/)。如果你认为光速测量是“地球圆阴谋”的一部分，请随意[做你自己的测量](https://hackaday.com/2016/09/29/testing-the-speed-of-light-conspiracy/)。

 [https://www.youtube.com/embed/SCF15sDD2IM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/SCF15sDD2IM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

