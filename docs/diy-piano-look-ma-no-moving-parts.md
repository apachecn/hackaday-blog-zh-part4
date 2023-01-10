# DIY 钢琴:看，马，没有活动部件

> 原文：<https://hackaday.com/2019/04/06/diy-piano-look-ma-no-moving-parts/>

[迈克尔·索伯拉克]对钢琴情有独钟，关注电容式触摸，对固态有着特殊的感情。这种头韵式的配方产生了一种 [DIY PCB 钢琴](https://www.instructables.com/id/PCB-Touch-Piano/),它省去了控制杆，也没有按钮，除非你算上 Teensy 上的库存重置按钮。一个真正坚持己见的人可能会指出扬声器有移动的锥体。除了这些有不动选项的切线部分，它是一个没有移动部件的电子仪器。

该项目的核心是一个 Teensy 3.2，它本身支持 12 个电容式触摸传感器。臭名昭著的演示板安装在自制的 PCB 上，有 12 个键，但实际上是一个不完整的八度音阶加上另一个高于第一个八度音阶的键。如果你仔细看，你已经注意到了丢失和多余的触摸板。在 Illustrator 中制作 PCB 走线是因为如果你有一个熟悉的工具，你就可以使用你所知道的东西，而且你不能说它是有效的。这个设计被转移到一个铜板上，使用的是我们喜欢的旧杂志页面技巧和可靠的旧铁酸。

我们不禁注意到，Teensy 的接线柱是焊接在电路板顶部的，而不是 IMT 式的钻孔。再说一次，结果说话，即使有改进的余地。据报道，有第二个版本的方式，其中包括每一个预期的关键。

 [https://www.youtube.com/embed/AInhi83X2z0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/AInhi83X2z0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



Via [PJRC 博客](https://www.pjrc.com/touch-piano-diy-circuit-board/)。