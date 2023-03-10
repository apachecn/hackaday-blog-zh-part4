# 应该用 555 或者 276 个

> 原文：<https://hackaday.com/2022/08/10/shouldve-used-a-555-or-276-of-them/>

当被要求制作一个简单的鸡蛋计时器时，我们大多数人可能会想到一个基于无处不在的 555 计时器的快速设计。在小小的八针 DIP 周围添加几个无源器件，在上面放置一个 LED 以显示时间用完，如果我们觉得有趣，甚至可以添加一个可变时间间隔的罐子。见鬼，我们很多人都能凭记忆做到。

那么，究竟为什么[杰西·法瑞尔]设法用巨大的 276555 做了基本上相同的事情呢？简单——因为为什么不呢？最初是作为我们 555 竞赛的最新版本[中的一个参赛项目开始的，【杰西】的目标很简单——只用 555 和必要的无源元件，建造一个带数字显示的功能计时器。他最终需要一些晶体管和二极管来实现它，但当你考虑到他用 555 替换了多少芯片，包括计数器、解码器、多路复用器和显示驱动器时，这是一个小小的让步。所有这些芯片都是由基本逻辑门、一个锁存器和一个触发器组成的，所有这些都是由一个或多个 555 或 556 或 558 等变体制成的。](https://hackaday.com/2021/12/01/the-555-timer-contest-returns/)

可想而知，276 个芯片占用了大量空间，完成定时器需要 11 块 PCB。一个主板充当计时器的控制面板，同时也充当十个其他卡的主板，每个卡专用于不同的功能块。一切都很整洁，而且执行得非常好，这与[Jesse]制作的优秀文档是一致的。整件事非常奇妙，不必要的复杂，我们非常乐意展示它。

 [https://www.youtube.com/embed/lylFiiJgOAI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/lylFiiJgOAI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

