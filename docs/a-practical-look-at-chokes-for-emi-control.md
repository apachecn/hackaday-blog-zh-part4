# 电磁干扰控制用扼流圈的实际应用

> 原文：<https://hackaday.com/2020/03/15/a-practical-look-at-chokes-for-emi-control/>

即使对那些有意钻研这一领域的人来说，射频电子学也像是一门黑色艺术。但是不幸降临到可怜的灵魂身上，他们只是偶然地不得不处理它，例如当寻求最小化电磁干扰时。[这本关于 RF 扼流圈如何降低 EMI 的初级读本](https://www.youtube.com/watch?v=84aKURxohlg)是从实用、注重结果的角度解释理论的好方法。

作为一名业余机械师和机床制造商，詹姆斯·克拉夫(James Clough)已经遇到了很多百代公司(EMI)令人厌恶的案例。变频驱动器是电磁干扰可能导致问题的一个地方，电机相位输出上的扼流圈通常是规定的。他在自己的一台机器上使用了一种昂贵的扼流圈，专门用于 VFD 应用，但他想知道一种廉价的铁氧体磁芯是否也能胜任这一工作，并着手寻找答案。

用借来的矢量网络分析仪扫描一些铁氧体磁芯并不令人满意，所以[James]用函数发生器和示波器做了一个简单的实验。他的演示展示了扼流圈的阻抗是如何随着测试信号频率的增加而增加的，这正是 VFD 中想要的行为——让相对低频的相位信号通过，同时阻挡高频 EMI。为了更好地测量，他将一个电容器与扼流圈并联，并展示了低通滤波器的优势。

我们喜欢这样的演示，它不仅仅是搔抓智力的痒处，而且还有一个实际的目标。[James]不仅展示了(至少在某些情况下)13 美元的铁氧体可以做与 130 美元的 VFD 扼流圈相同的工作，而且他展示了它们是如何工作的。这是最基本的东西，但也是你继续学习更高级的 RF 滤波器设计所需要知道的。

 [https://www.youtube.com/embed/84aKURxohlg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/84aKURxohlg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

