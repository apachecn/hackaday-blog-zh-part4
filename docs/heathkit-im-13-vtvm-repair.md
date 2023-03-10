# 希斯基特 IM-13 VTVM 修理

> 原文：<https://hackaday.com/2021/11/07/heathkit-im-13-vtvm-repair/>

如果你不到一定的年龄，你可能不知道 VTVM 的首字母。它代表真空管电压表。乍一看，你可能会认为这是“老式电压表”的简称，但事实上，VTVM 在过去的测量仪器中扮演着重要的角色。【无线电机械师】[带我们进入一个需要一些爱](https://www.youtube.com/watch?v=HOLeFLK_Tvo)的希斯基特 IM-13，对它来说，这是一个令人印象深刻的小仪器。

如今，我们的电表几乎总是有一个 FET 前端，并且可能使用 MOSFET。这意味着电压测量探头根本没有真正连接到电表上。在正常工作的 MOSFET 中，栅极和电路其余部分之间的 DC 电阻实际上是无穷大。更有可能是一个非常大的电阻(如 10 兆欧)在设置输入阻抗，因为栅极本身可能会拾取静电电压，从而损坏器件。这样的高电阻在测量时非常有用，因为它不太可能干扰您要测量的电路，并且可以实现更精确的测量。

我们今天认为这是理所当然的，但在过去，一个典型的电压表只是一个前面有一些电阻的仪表。虽然一个好的电表具有相对较高的电阻，但它没有 FET 高。然而，对于电子管放大器，VTVM 也可以表现出非常高的电阻，并且仍然可以进行良好的测量。Heathkit 电表使用双管作为放大器，并配有一些输入电阻分压器，以提供 11 兆欧的输入。还有一个整流管接入进行交流测量。最终，放大器驱动传统的模拟仪表，但该负载与被测器件隔离，因此其相对较低的电阻并不重要。

修复看起来很简单，但看到其中一个的内部很有趣。把它比作今天的数字仪表，看起来很奇怪，不是吗？如果你想了解更多关于虚拟仪器是如何使用的，网上有一本关于虚拟仪器的 1951 年的书[。一些人仍然](http://www.cfp-radio.com/documentations/Sylvania-VTVM.pdf)[喜欢移动的仪表](https://hackaday.com/2017/11/08/why-you-shouldnt-quite-forget-the-moving-coil-multimeter/)，我们承认，对于某些任务，它们甚至胜过数字条形图。

 [https://www.youtube.com/embed/HOLeFLK_Tvo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/HOLeFLK_Tvo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

