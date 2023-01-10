# 五轴 3D 打印让世界变平

> 原文：<https://hackaday.com/2021/01/12/3d-printing-in-five-axes-makes-the-world-flat/>

就在你认为你的 3D 打印机很热门的时候，5D 打印机出现了。宾夕法尼亚州立大学的两名博士生想要[再增加两个轴](https://www.sciencedirect.com/science/article/abs/pii/S2214860420309416)来消除突出物。这意味着，打印机不是支撑物体或将物体分成碎片，而是简单地确定打印方向，使零件的每个区域都像平面一样打印。当然，5D 打印机并不是真正的新东西，尽管你不太听说过它们。然而，该论文详细描述了一种新算法，该算法消除了手动定义印刷区域和旋转。

当你设置打印时，你总是手动这样做。例如，如果你想打印一个字母 T，你可以在横条下用支撑打印它，或者把它翻转过来，在没有支撑的情况下打印它。这里的区别是打印机可以将工件翻转到不同的角度，并可以在打印过程中随时改变它。打印机可能会打印 T 的轴，旋转它以绘制横杆的一半，然后将其旋转 180 度以打印另一半。在所有三个区域中，打印头都将材料沉积平整，没有突出物。在像 T 这样的简单情况下，不需要特殊的机器或算法，但在一般情况下，你不能只旋转模型来避免使用支撑。

所提出的算法可以考虑打印机可以处理多少悬垂角，以便它可以尽可能少地重新定向模型。据推测，与仅铺设新层相比，旋转打印相对耗时。

我们真的很想看一张 5D 机器运转的照片，但是我们没有找到任何实际的照片。然而，下面的视频是一台商用 5D 机器——想必你必须手动设置它——它还展示了一个零件如何旋转以获得平面打印的好例子。老实说，我们不确定论文中的算法是否已经应用于真实的印刷品。照片看起来不像模型实际上是 3D 打印的。

我们不得不怀疑 5D 是否能进入消费 3D 打印市场。然后，市场宣传将会开始，我们将会有由市场部驱动的 20D 打印机。

这让我们想起了 [2.5D 打印](https://hackaday.com/2019/09/09/hows-that-2-5d-printer-working-for-you/)，但其实不是一回事。如果你的部分在旋转，它可能会为[的床粘连](https://hackaday.com/2018/11/05/better-3d-printing-through-magnets/)增加一个全新的悲伤水平。

 [https://www.youtube.com/embed/5z2dk0H5mZU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/5z2dk0H5mZU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

