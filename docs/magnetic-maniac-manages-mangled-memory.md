# 磁性狂人管理损坏的内存

> 原文：<https://hackaday.com/2022/09/04/magnetic-maniac-manages-mangled-memory/>

啊，软盘。很少有东西能像软盘一样承载怀旧之情——312 或 514，取决于你是哪一代黑客。(是的，我们听说你有灰胡子，8 英寸软盘绝对是一件事。)真正的好东西不是软盘本身，而是它们所携带的东西，如 Wolfenstein 3d、Commander Keen、DOS 或任何其他过去的经典产品。不幸的是，一堆软盘不再承载任何东西，因为它们最终会坏掉。更糟糕的是，在一些损坏的软盘上，格式化操作也会失败。当然，这些软盘是注定要被扔进垃圾箱的，对吗？

好吧，等一下。[AnotherMaker] [发现了一种可能给那些死气沉沉的磁盘注入更多生命的东西](https://www.youtube.com/watch?v=49Pcmgh7tPc)——磁铁！具体来说，他正在使用消磁器，即现实的大容量磁带橡皮擦，尽管足够长的时间用强磁体可能也会起作用。彻底处理磁盘，将它放回老式机器中，很有可能它会愉快地格式化。现在剩下的就是找出原因。

这是对齐问题吗？在对齐问题中，多个驱动器在略有不同的位置写入数据，即使在写入磁头开始格式化后，读取磁头仍会拾取这些错误区域。或者也许磁盘上有一个点变坏了，需要更强的磁场来重置软盘的磁场。让我们知道您的猜测，或者如果您知道答案，请告诉我们！

 [https://www.youtube.com/embed/49Pcmgh7tPc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/49Pcmgh7tPc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

