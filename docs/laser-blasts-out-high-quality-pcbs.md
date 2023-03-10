# 激光爆破出高质量的多氯联苯

> 原文：<https://hackaday.com/2021/01/11/laser-blasts-out-high-quality-pcbs/>

随着定制印刷电路板变得如此便宜和快速，它几乎没有意义再推出自己的，特别是当你考虑到凌乱的蚀刻步骤和不太好的结果。当然，这不是制造 PCB 的唯一方法，如果你碰巧有 20 瓦的光纤激光器，你可以得到一些很难从商业电路板上分辨出来的奇妙的自制 PCB。

Lucikly，Kurokesu fame 的[Saulius Lukse]手头就有这样一台激光器，通过良好的工具链和一些妥协，他能够在 30 分钟内生产出 0.1 毫米间距的 PCB。折衷方案包括单面电路板和无通孔，但这仍然允许许多不同的有用设计。该过程从 Gerbers 通过 FlatCAM 开始，然后导入 EZCAD 进行激光加工。在激光开始烧掉走线之间的铜之前，有相当多的手动调整，对于 FR4 上 0.035 毫米的箔片来说，这需要大约 20 次。我们不得不承认，在下面的视频中观看切割过程非常酷。

一旦走线被切割，紫外线固化阻焊适用于整个板。固化后，电路板再次回到激光器，暴露焊盘。最后几道激光关至 11 度，将完成的纸板切割下来。我们想知道为什么激光不用来钻孔；我们知道过孔很难连接到另一侧，但似乎可以支持通孔元件。也许这就是[Saulius]最终的目标，因为有迹线终止于似乎是通孔焊盘的地方。

不管目标是什么，这些板子真的很光滑。我们通常看到[激光在传统蚀刻之前用来去除抗蚀剂](https://hackaday.com/2017/08/22/laser-etching-pcbs/)，所以这是一个很好的改变。

 [https://www.youtube.com/embed/-dQzufH8FEQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/-dQzufH8FEQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

