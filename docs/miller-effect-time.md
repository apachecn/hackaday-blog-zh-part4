# 米勒(效应)时间

> 原文：<https://hackaday.com/2021/07/21/miller-effect-time/>

虽然[米勒效应](https://www.youtube.com/watch?v=czk0I3ga3LQ)听起来可能很有趣，但它实际上是放大器中寄生电容的效应。你会怎么做？观看[所有电子产品]下方的视频，了解详情。我们喜欢它使用的测试电路有一个开关，用于将缓解电路放入和取出测试，以进行比较。

实际上，米勒效应可以指任何阻抗，但实际上，由于电子管和晶体管的结构，它通常是寄生电容。有时微小的电容会被该级的反相增益放大，从而增加放大器的输入阻抗。这进而降低了该级的带宽。

米勒效应有很多细微差别。当然，你可以像视频指出的那样中和它。您也可以在放大器的输入或输出端使用同相缓冲器来降低这种影响。一些设计师还利用这一效应将小电容转换成大电容，尤其是在 IC 设计等难以制造大电容的应用中。

通常，输出电容被忽略，因为总输出阻抗幅度很小。但是，如果你有一个高阻抗输出，它也需要纳入分析。

我们谈到了[晶体管偏置](https://hackaday.com/2018/05/11/biasing-that-transistor-the-common-base-amplifier/)，评论中提到了米勒电容。当然，你在[旧电子管电路](https://hackaday.com/2018/06/22/the-history-and-physics-of-triode-vacuum-tubes/)中也得到了同样的效果。

 [https://www.youtube.com/embed/czk0I3ga3LQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/czk0I3ga3LQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

