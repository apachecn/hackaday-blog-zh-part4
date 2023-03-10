# 驱动谢妮电子管的更好方法

> 原文：<https://hackaday.com/2018/08/22/better-ways-to-drive-nixie-tubes/>

啊，谢妮电子管。除非你身边有几个谢妮电子管，否则你就不酷，除非你有自己的数码管时钟，否则你就不牛逼。这就是[Thomas] [为了参加 Hackaday Prize](https://hackaday.io/project/69708-low-cost-dual-nixie-driver) 正在做的事情，他想出了一个非常低成本的方法。

对于这个建筑的高压电源，[Thomas]正在转向基于 MC34063 的标准电路之一，它足够简单，足够好，可以让一切工作。这里的供电真的没有什么惊喜。不过，这完全是一个关于打开谢妮内部不同数字的项目，为此[Thomas]开发了自己的电路板，能够用一台 ATMega8 驱动一对二合一 Nixies。

这两个谢妮板通过 UART 连接以菊花链形式连接在一起，每个板通过线路传递数字。例如，第一个电路板接收 12、30 和 59，显示 59，并将 12 和 30 向下传递到下一个电路板。然后，第二块板显示 30，并将 12 传递给最后一块板。

当然，如果你已经设计了一个谢妮驱动程序，接下来要做的就是构建一个时钟。[托马斯]有一个相当聪明的想法，用 3D 打印的内部模具，用混凝土为这个钟做一个外壳。一切似乎进行得很顺利，直到是时候把内部模具拔出来了，轻轻敲了几下就出现了一些相当大的裂缝。这是令人失望的，但随着轻微的重新设计和一些更多的混凝土混合纤维，这将是一个重要的胜利。

The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)