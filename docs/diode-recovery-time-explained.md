# 二极管恢复时间解释

> 原文：<https://hackaday.com/2018/07/11/diode-recovery-time-explained/>

学习电子学至少有两个阶段。在第一阶段，您将了解组件应该如何工作。在第二阶段，你将了解它们是如何真正工作的。导线有电阻和电感。相邻导线有电容。电容漏电。电感有电阻。所有这些都很重要。[Learnelectronics]最近有一个视频，[探索了二极管](https://www.youtube.com/watch?v=CVzPOf8gwh4)的恢复时间——第二阶段的对话。

如果你以前没有遇到过恢复时间，那就是二极管导通后关断的时间。这表现为一点点下冲，二极管应该阻挡的信号会短暂泄漏。

视频着眼于不同频率下的几种不同类型的二极管。恢复时间对包括[开关电源](https://hackaday.com/2018/07/06/circuit-vr-simple-buck-converters/)在内的几种设计都有影响。如果你深究物理学，通常会在其他几个参数和恢复时间之间进行权衡。为了让您有个概念，BAT42 肖特基二极管的数据手册说，10mA 下的反向恢复时间不超过 5 ns。

视频显示了反向恢复时间，但正向恢复时间也是一个问题，尽管这通常不是一个大问题，除非你处理非常高的电流。如果你想要更专业的解释，可以阅读来自 [Vishay](https://www.vishay.com/docs/84064/anphyexp.pdf) 和 [Fairchild](https://www.fairchildsemi.com/technical-articles/Understanding-Diode-Reverse-Recovery-and-Its-Effect-on-Switching-Losses.pdf) 的应用笔记。

如果你想对同一个主题有不同的看法，[w2ew]不久前也做了一个关于这个主题的视频。

 [https://www.youtube.com/embed/CVzPOf8gwh4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/CVzPOf8gwh4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

