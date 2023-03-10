# 以 1970 年的方式对磁盘驱动器进行条带化

> 原文：<https://hackaday.com/2022/05/16/striping-a-disk-drive-the-1970-way/>

如今，计算机的大容量存储非常简单。它要么使用转盘，要么是固态的。也有一些坚持使用磁带的人，但与过去相比，磁带几乎是死的。但就在不久前，海量存储还有很多种。磁带、磁盘、磁鼓、穿孔卡片、纸带，甚至更奇怪的东西。也许没有什么比 IBM 2321 数据单元驱动器更奇怪了，IBM 内部称之为 MARS。

你可能会问什么是数据单元？数据单元是 IBM 在 1964 年推出的一种大容量存储设备，使用看起来像一英尺左右的摄影胶片的磁条，可以存储大约 400 兆字节。这些条带位于一个可以旋转的滚筒内。当你需要一张唱片时，鼓会将你需要的带子旋转到工作部分，一个自动化的过程会将有问题的带子取出，缠绕在读/写头上，然后在完成后放回原处。

不用说，这些没有流行起来。磁带驱动器对大多数事情来说都很好，磁盘驱动器将很快变得更便宜，这注定了 2321 将成为历史的奇迹。

然而，考虑到当时的限制，这个解决方案是聪明的。每一条都是两英寸多一点宽，13 英寸长。每个磁鼓上有 200 个磁带，一个 20 磁道的磁头可以移动到五个位置之一，这意味着每个磁带可以存储 100 个磁道的数据。对于高存储需求，您可以将多个设备连接在一起。

[![](img/72623d327155c679d00a900217c57bb4.png)](https://hackaday.com/wp-content/uploads/2022/05/ibmcell.png)

The drum was like a very tall slide projector carrying magnetic strips instead of optical slides

如果你看图片，很难看出 200 条怎么能装进桶里。你必须看看 IBM 手册中的图，这就清楚了。鼓实际上是由 10 个单元组成的。每个单元有两个 10 条的子单元。物理排列就像一个旧的旋转幻灯机。这些条带就像非常薄的馅饼片，机器将一个特定的条带吸入固定的读写头。

当然，这看起来有点像鲁布·戈德堡，但是想想这个。当时类似的 IBM 磁盘驱动器的容量还不到数据单元容量的 1/50。如果您在一个控制单元中装入八个鼓，那么它将相当于 440 多个 IBM2311 磁盘驱动器。别忘了，磁盘驱动器也需要 50 个以上的控制器。磁盘驱动器当然更快，但也快不了多少。2311 的存取时间为 85 毫秒，而数据单元在最差情况下的时钟时间约为 600 毫秒，但如果星形和条形对齐，最快可达 95 毫秒。

[![](img/541cd0f7ec0a7b135fb55779649efeae.png)](https://hackaday.com/wp-content/uploads/2022/05/cart.png)

Tape cartridge for the IBM 3850

如果你认为这些很吵，那你就对了。他们还用一种特殊的油来润滑所有的机件。显然[Nerding]在过去有机会与其中一个一起工作。电脑在授予和拒绝信用授权，它一直被挂起。事实证明，共享这些数据单元是有风险的。一个程序将移动磁鼓，另一个程序将再次移动磁鼓，然后第一个程序才能读取这些程序是否正在访问磁鼓的相对面。

IBM 还生产了可以在 IBM System/370 上存储高达 472 GB 的 3850。这是一个非常相似的想法，但磁带不是条状的，而是在每个大约 50 MB 的小磁带盒中。虽然这更像是一台自动化的磁带机，而不是磁盘驱动器，但它仍然表明磁盘需要一段时间才能完全取代磁带。

[![](img/427180f7d41dea6974ad4fb81fbbf117.png)](https://hackaday.com/wp-content/uploads/2022/05/heads.png)

IBM’s diagram of the read/write head

我们有一种轻微的冲动，想建造一个可以工作的复制品。当然，在 1.8 度上排队涉及一些精度，但如果你建造 3D 打印机或 CNC 机器，这个数字肯定有一个熟悉的环。典型的步进电机恰好每转 200 整步。去想想。另一件很难准确做到的事情是处理那层薄薄的薄膜。据 IBM 称，薄膜本身的厚度为 0.005 英寸。尽管如此，你还是认为你能想出办法。

我们会满足于一个[模拟器](https://hackaday.com/2019/05/02/a-mainframe-tape-drive-emulator/)，特别是如果它有一个图形模拟的话。虽然我们可能要感谢 IBM 普及了磁带存储，但我们也要感谢[宾·克罗斯比](https://hackaday.com/2018/08/07/recorded-programming-thanks-to-bing-crosby/)让录音带成为现实。