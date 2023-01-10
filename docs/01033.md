# $3 万用表拆卸

> 原文：<https://hackaday.com/2018/10/23/3-multimeter-teardown/>

[疯狂二极管]和他的猫决定看看一个 3 美元的电表是如何工作的。仪表上标有 DT-830B，而他已经有了一个相同型号的旧仪表，他想知道他们怎么能以 3 美元的价格出售它(包括运费)。你可以在下面看到他的[测试、拆卸和逆向工程](https://www.youtube.com/watch?v=R693vS09hoo)的视频。

奇怪的是，尽管型号相同，电表的尺寸却有点不同。当他打开外壳安装电池时，他注意到电路板看起来没有适合额定电压的保险丝或组件。他断定丢失的零件可能在板子下面，并测试了仪表。

平心而论，3 美元的价格，这个计价器和他的其他计价器相当吻合。交流标度看起来只不过是为 DC 计供电的二极管，只是工程单位转换系数略有不同。这不是最准确的方法，但肯定符合你对 3 美元电表的期望。然而，后来，外壳和 PCB 出来了，在电路板的另一侧没有额外的元件。

最初的 DT-830B 在需要的地方有结实的电阻，最重要的是，有一个用于电流测量功能的保险丝。新的那台在外壳上有一个关于它使用的保险丝类型的标记，但里面没有保险丝，尽管有可能是保险丝的 PCB 焊盘。

也许那些部分是不必要的？画出原理图后，视频显示，事实上，电压和功耗确实需要更大的元件。此外，连接错误很容易给 IC 带来非常高的电压。

这看起来很像我们不久前看到的 DT-832。那一个有一个保险丝，但是，我们不知道它是否有更好的额定电阻。我们也看到过带保险丝的廉价电表[实际上并未使用](https://hackaday.com/2015/06/02/fail-of-the-week-the-deadliest-multimeter/)。

 [https://www.youtube.com/embed/R693vS09hoo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/R693vS09hoo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

