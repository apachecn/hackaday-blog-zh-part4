# 老式乐器用现代方式取代了非乐器部件

> 原文：<https://hackaday.com/2020/07/10/vintage-instrument-gets-modern-replacement-for-unobtainium-parts/>

Hackaday 最棒的一点是，你能从人们处理的项目中学到多少东西，尤其是当他们在修复具有未知故障模式和潜在多重问题的旧设备时。同样，黑客日最糟糕的部分是看到其他人的能力，并且知道你还有很长的路要走才能赶上他们。

一个恰当的例子是[【好奇的马克】最近修理了一个旧的脉冲发生器](https://www.curiousmarc.com/instruments/hp-8082a-pulse-generator)。问题中的仪器是一台 H-P 8082A，正如[马克]如此雄辩地指出的那样，在那个时代，惠普是一个“由更好的工程师管理的好工程师[想要]帮助其他工程师”的地方。该仪器能够输出 250 MHz，完全控制脉冲的幅度、频率、占空比以及上升和下降沿几何形状，此外还能够输出双脉冲。对于 1974 年制造的全模拟仪器来说，它的状态还不错，而且它仍然通电，至少产生方波输出。但是[马克]的探索揭示了一些问题，这些问题在下面的第一个视频[中有详细的和部分的说明。](https://www.youtube.com/watch?v=09zhUbJl37w)

在[第二部分](https://www.youtube.com/watch?v=gNtZOD6zl1k)【Marc】探讨脉冲延迟功能背后的问题。他追踪到一个坏的 IC，这是一个坏消息，因为它是一个定制的惠普部件，使用发射极耦合逻辑(ECL)来实现所需的性能，这种性能不再能够获得。所以很自然地，[马克]决定用定制电路替换芯片。第二部分详细介绍了电路的设计和仿真，而设计 PCB 以处理高速信号的重要细节占据了第三部分的大部分[。我们发现获得走线阻抗的细节非常有趣。](https://www.youtube.com/watch?v=PuzbwwIN85U)

最终，[马克]的脉冲发生器被打捞上来。它将投入使用，帮助他探索阿波罗时代老式电子设备的奥秘，所以我们期待看到更多关于这个伟大的古老仪器的信息。

 [https://www.youtube.com/embed/09zhUbJl37w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/09zhUbJl37w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/gNtZOD6zl1k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/gNtZOD6zl1k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/PuzbwwIN85U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/PuzbwwIN85U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

