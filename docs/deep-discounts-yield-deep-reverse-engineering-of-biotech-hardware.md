# 大幅折扣产生了生物技术硬件的深度逆向工程

> 原文：<https://hackaday.com/2019/01/15/deep-discounts-yield-deep-reverse-engineering-of-biotech-hardware/>

对于我们的大多数读者来说，逛电子剩余产品商店可能已经是老生常谈了。在某个地方，每个人都有那一小堆他们将来肯定会用到的硬件。旧传真是一回事，但如果你把一整个托盘大小的基因测序仪带回家，你的伴侣会怎么想？我们的朋友[kaspar]发来了一个有趣的消息，瑞士黑客空间 hacketeria[的人去年得到了一台 Illumina HiSeq 2000](https://reseq.hackteria.org/) (见有趣的“看我们得到了什么！”上面的照片)并且已经生成了[大量关于里面是什么以及如何使用它的公开文档](https://www.hackteria.org/wiki/HiSeq2000_-_Next_Level_Hacking)。

[![](img/be609577bf9054b689c349e6efeade69.png)](https://hackaday.com/wp-content/uploads/2019/01/img_20180201_223556-e1547419813867.jpg)

好吧，首先，这到底是什么机器？HiSeq 旨在自动执行 Illumina 专有的多步骤基因测序过程的测序步骤([参见制造商的说明书](https://www.illumina.com/documents/products/datasheets/datasheet_hiseq2000.pdf)了解更多信息)，并在最少的人工干预下完成。这意味着该单元包含一个操纵样品的微流体系统，一个具有可控载物台、成像仪、荧光模式等的极高性能光学扫描系统，以及许多其他作者没有足够训练来猜测的东西。

Hackteria 的人对系统进行了彻底的拆解，并制作了大部分模块的框图。他们还运行了一些工具，并记录了他们正在做的事情，包括发送到机器和从机器接收的串行命令，以控制某些子系统。当然，像这样的工具是由 Illumina 的特定软件驱动的，但这些软件通常是可用的，并且令人惊讶地可用，这就是前面提到的日志是如何被捕获的。现在看来，Hackteria 已经组装好工具，让[将该系统用作荧光显微镜](https://www.hackteria.org/wiki/HiSeq2000_-_Next_Level_Hacking#Using_the_HiSeq2000_as_aFluorescent_Scanning_Microscope)。 [![](img/3362f43383529135afd27e2cda54ff07.png)](https://hackaday.com/wp-content/uploads/2019/01/hiseqopticalsystem.png)

奇怪的是，这里最有趣的事情可能是这些系统的可用性。似乎它们正在被大量替换，在二级市场上很容易买到，价格在几千美元左右。在这个价格点上，他们几乎值得抢购的外壳和零件！但我们更喜欢 Hackteria 的目标，即让公民科学家能够利用这些不可思议的机器实现他们的预期目的。谁知道当黑客开始给他们的猫测序时，我们会发现什么令人兴奋的项目！

感谢提示[[kaspar](https://github.com/kasbah)]！