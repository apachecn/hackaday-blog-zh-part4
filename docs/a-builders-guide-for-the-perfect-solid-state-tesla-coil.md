# 完美固态特斯拉线圈建造指南

> 原文：<https://hackaday.com/2021/10/31/a-builders-guide-for-the-perfect-solid-state-tesla-coil/>

[扎克·阿姆斯特朗]为您呈现了一个简单的指南，让您享受制作固态特斯拉线圈的乐趣。该设计基于使用 [UCC2742x](https://www.ti.com/lit/ds/symlink/ucc27425.pdf) 栅极驱动器 IC 的自谐振设置，该 IC 用于变压器耦合全波配置，从线路输入提供最大功率。自谐振位是通过使用线圈附近的小天线来拾取 EM 场，并通过适当地箝位和平方它来实现的，它被反馈到栅极驱动器以闭合反馈环路。这种合理的设置允许电路与各种特斯拉线圈设计一起振荡，并跟踪任何微小的变化，最大限度地减少对精细手动调谐的需要，这是你建造这些东西的通常途径。

由于初级由[IGBT](https://datasheet.octopart.com/FGA60N65SMD-Fairchild-Semiconductor-datasheet-68791176.pdf)驱动，因此越大越好。如果线圈太小，谐振频率将超过建议的 400 kHz，这可能会损坏 IGBTs，因为它们无法在所需的相对较大的电流下更快地切换。设计 Tesla 线圈驱动器电路的一个重要部分是使初级线圈与驱动器匹配。你可以做得比检查[javac](http://www.classictesla.com/java/javatc3d/javatc3d.html)更糟来帮助计算，因为这是一个错误经常导致破坏性失败的设计领域。次级线圈设计更简单，只需做一点实验就能获得合适的线圈耦合度。太多的耦合是没有帮助的，因为你只会得到双方之间的崩溃。太少的耦合和效率会受到损害。这就是为什么你经常看到特斯拉线圈的初级和次级线圈之间有相当大的间隙。这种魔法是有科学依据的！

![](img/dda6b7d0dc31266c380af360c774286a.png)

Pretty Lithium Carbonate plasma

一个 555 定时器有线产生可调脉冲馈入驱动器使能允许轻松改变放电属性。这使得它能够在一个极端产生看起来有点像范德格拉夫放电的放电，并在另一个极端产生一些可爱的等离子体“火”。

多年来，我们从许多角度报道了特斯拉线圈，最近这个[等离子高音喇叭发出甜美的声音](https://hackaday.com/2021/06/19/is-it-a-plasma-tweeter-or-a-singing-tesla-coil/)，不知何故，我们错过了由【StyroPyro】制造的[疯狂危险的特斯拉，只是从远处检查旋转火花隙。](https://www.youtube.com/watch?v=Oij-BdIkPgQ)

 [https://www.youtube.com/embed/zCf-PwXsG_E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/zCf-PwXsG_E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

