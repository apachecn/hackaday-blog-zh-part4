# Fluke DMM Hack 在型号上增加了一位数字

> 原文：<https://hackaday.com/2022/02/07/fluke-dmm-hack-adds-one-digit-to-model-number/>

在他众多的兴趣中，[达夫·琼斯]喜欢测试和测量设备。他最近在他的电子博客上发布了几个视频，探索福禄克电压表如此昂贵的原因。在这个过程中，[他偶然发现了一个有趣的针对 Fluke 77](https://www.youtube.com/watch?v=X_1M3xgl4zo) 的黑客攻击。

福禄克 77 是在 1983 年推出的，是交流模式下的平均响应仪表。这种型号已经成为维护站和实验室中使用寿命很长的设备的事实标准，例如，军事和工业设备。围绕 Fluke 77 的使用设计了许多测试程序和培训材料。当一个新的更好的仪表出现时，改变它们的成本通常是如此之高，以至于它们还不如被铸在石头上——或者至少被 WordStar 驱动的菊花轮打印机锤成 20 磅的扇形纸。但对于那些没有这种遗留要求的人来说，福禄克从本世纪初就有 17x 系列的真有效值读数表。这些电表与其 7x 系列的同类产品在视觉上非常相似，除了交流测量方法之外，基本上可以互换。

![](img/00d732dfc33289fa9961fcbadfcd5078.png)

在拆除 Fluke 77 米的过程中，完全出于另一个原因，[戴夫]发现相似之处不仅仅是视觉上的。不仅 77 的 PCB 标有 17x，而且板上还有 ADI 公司的 AD737 真均方根-DC 转换器 IC。

> 怎么回事？他们为什么要花钱把这个芯片放在一个普通的响应仪表中呢？

再深入研究一下[，数据手册](https://www.analog.com/media/en/technical-documentation/data-sheets/ad737.pdf)显示该芯片可以在三种不同模式下测量:真有效值、平均整流或绝对值。选择真有效值模式只需增加一个 33 uF 电容。果然，在福禄克示意图中，这清楚地显示为一个可选负载。

毫不奇怪，[戴夫]做了修改，它的工作。唯一的缺点是，在你做了这种改变之后，你必须对血糖仪进行一次完全的重新校准。例如，令人烦恼的是，似乎没有任何方法可以校准交流测量。除非你是一个像[Dave]一样的测试设备上瘾者，否则你可能没有所有的设备来自己执行这种校准——如果你在家里尝试这种方法，请记住这一点。另一件要注意的事情是，这次黑客攻击是在现代福禄克 77 四米。如果你有一个 1985 年的 Fluke 77，这个黑客并不适用。

 [https://www.youtube.com/embed/X_1M3xgl4zo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/X_1M3xgl4zo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

