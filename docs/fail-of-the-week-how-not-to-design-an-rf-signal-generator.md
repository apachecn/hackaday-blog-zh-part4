# 本周失败:如何不设计射频信号发生器

> 原文：<https://hackaday.com/2018/09/06/fail-of-the-week-how-not-to-design-an-rf-signal-generator/>

我们通常会把本周失败的荣誉留给我们中的一个人——一个在板凳上苦干的人，或者一个差点获得达尔文奖的人。我们一般不会在 FotW 中突出商业产品，但是在[这个不合标准的射频信号发生器](https://www.youtube.com/watch?v=Cj-mYhmI2fc)的情况下，我们会破例。

我们假设失败的徽章在某种程度上可以被钉在[电子更新]上；毕竟，他花了 200 美元买了 RF Explorer 信号发生器，它的覆盖范围从 24 MHz 到 6 GHz。但在真正的柠檬到柠檬水的时尚，下面的视频他为我们提供了一个单位的性能和拆卸单位的彻底分析。

第一步是用频谱分析仪观察信号，这并不令人鼓舞。如果该单元产生一个纯正弦波，我们就不会看到指示整个频带谐波的尖峰森林。示波器也好不到哪里去；波形更接近方波，而不是正弦波。在引擎盖下，他发现了一个 PIC 微控制器和一个 MAX2870 频率合成器，但明显缺少任何 RF 滤波组件，这解释了输出为何如此粗糙。诚然，与频率范围如此之宽的实验室级信号发生器相比，200 美元并不算多。当然，外部过滤器会有所帮助。但是对于 200 美元来说，期待至少一些过滤似乎是合理的。

我们赞赏[electronupdate]为我们的团队提供了一些有价值的 RF 设计建议。我们习惯于看到他拆卸元件，比如[这个窥视表面贴装电感](https://hackaday.com/2017/05/24/what-lies-within-smt-inductor-teardown/)的人，但我们也喜欢像这样深思熟虑的评论。

 [https://www.youtube.com/embed/Cj-mYhmI2fc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Cj-mYhmI2fc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

