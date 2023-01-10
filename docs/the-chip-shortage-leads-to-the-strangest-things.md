# 芯片短缺导致了最奇怪的事情

> 原文：<https://hackaday.com/2022/08/13/the-chip-shortage-leads-to-the-strangest-things/>

全球芯片短缺并没有让电子设计工程师的生活变得轻松，因为产品是围绕任何可用的部件而不是首选部件来设计的。这已经以一些意想不到的方式表现出来，包括[CNX 软件]调查的[产品，其多项选择的物料清单导致制造过程中出现错误](https://www.cnx-software.com/2022/08/10/another-consequence-of-supply-shortage-mass-production-mishaps/)。

从表面上看，设计一个具有两组尺寸的 PCB 以适应多种器件选择是一个明智之举。但是正如 Radxa 在他们的 Rock 3A 单板计算机中发现的那样，这可能会导致生产事故，因为一些板离开生产线时，其 USB PD 电路中出现了混搭 BoM[，这使它们无法在 5 V 以上的电压下工作](https://forum.radxa.com/t/rock-3a-product-defect-notice-batch-2022-04-22-2022-06-15/11088)。电路板上有一个集成电路和一个 WCH 器件，故障电路板上的支持元件似乎是为电路板上的另一个芯片安装的。

我们和[CNX]一起祝贺 Radxa 坦白，我们希望解决这个问题的一个办法是给它送去适合自己的芯片。我们很高兴不是在我们的监督下发生了这样的错误，因为从经验中我们知道这些事情很容易发生。

芯片短缺在你的生活中有没有导致过类似的生产失误？请在评论中告诉我们。