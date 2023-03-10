# 互联网——在卡西欧计算器上！

> 原文：<https://hackaday.com/2021/07/18/the-internet-on-a-casio-calculator/>

多年来，我们已经习惯于看到一些令人印象深刻的高端计算器软件和硬件的黑客，最常见的是与德州仪器(Texas Instruments)基于 Z80 的型号有关。但是当然，TI 远不是这个竞技场上唯一的玩家。看到卡西欧受到一些关注，这是一种改变。卡西欧 fx 系列图形计算器现在可以与世界交流，这要归功于[Manawyrm]在[向它们移植 TCP/IP 堆栈](https://github.com/Manawyrm/fxIP#readme)的工作。

从下面的视频中可以看出，潜伏在计算器菜单系统中的是一个 IRC 客户端，还有[一个终端应用程序](https://www.youtube.com/watch?v=epFX8K0dhdY)和一个网络服务器[，你甚至可以在线访问它们](http://fxip.as203478.net/)(请注意，它只是一个计算器，所以黑客读者点击链接的攻击可能会使它崩溃)。卡西欧没有自己的网络接口，所以它通过串行端口说话。在这次尝试中，它使用了来自[ [托布勒米纳](https://github.com/TobleMiner) ]的 UART 驱动程序。

看到一个被忽视的平台得到一些爱总是好的，并且注意到这是一个不寻常的 SH4 CPU 在其最熟悉的 Sega Dreamcast 之外的一次外出。令人惊讶的是，在所有产品的计算器中，[的 SH4 是一个缺少 FPU](https://en.wikipedia.org/wiki/SuperH#SH-4_2) 的定制版本。这个缺陷并不意味着它不能超频，正如这篇非常古老的 Hackaday 文章所描述的[。](https://hackaday.com/2007/08/01/how-to-overclock-a-casio-fx-9750g-plus/)

 [https://www.youtube.com/embed/afkrucsMMrc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/afkrucsMMrc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

