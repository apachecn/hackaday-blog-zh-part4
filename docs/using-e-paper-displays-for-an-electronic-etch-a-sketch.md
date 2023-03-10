# 使用电子纸显示器进行电子蚀刻草图

> 原文：<https://hackaday.com/2018/11/09/using-e-paper-displays-for-an-electronic-etch-a-sketch/>

电子产品通常在复制非电子产品时最成功。因此，大多数屏幕都不是纸张的好替代品。当然，除了电子纸。这些显示器即使在阳光下也具有高对比度，并且即使没有电源也能保持图像。当[smbakeryt]在看他女儿的蚀刻草图时，他决定复制它的操作将是一个了解这些纸状显示器的好方法。

你可以在下面看到他的结果和发现的视频。他买了几个显示器，并展示了所有这些显示器，包括一些添加单一专色的三色单元。你会注意到的一件事是显示器很慢，这可能是它们没有占领世界的原因。

显示器连接到 Raspberry Pi，许多显示器可以直接安装到 Pi 上。最大的显示器接近 6 英寸，一些较小的显示器甚至可以弯曲。似乎三色显示器比使用两种颜色的显示器要慢得多。为了应对缓慢的更新速度，一些显示器可以支持部分刷新。

这个绘画玩具使用连接到树莓派的光学编码器。 [Python 代码](https://github.com/sbelectronics/sketch)可用。即使你不想复制玩具，显示器的对比也值得一看。我们真的希望他包括一个加速度计，通过摇动来消除它，但你必须自己添加这个功能。顺便说一下，在视频中，他提到真正的蚀刻素描可能与磁铁一起工作。并没有。这是一种铝粉，它会粘在塑料上，直到一支铁笔把它擦掉。

当然，我们以前已经多次看到过这些展示。如果你有足够的耐心，你甚至可以将它们用作 [Linux 显示器](https://hackaday.com/2018/08/14/run-a-linux-terminal-on-cheap-e-ink-displays/)。

 [https://www.youtube.com/embed/RoYZxaUZues?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/RoYZxaUZues?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

