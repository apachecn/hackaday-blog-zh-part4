# 卫生纸的准确分发将帮助我们度过危机

> 原文：<https://hackaday.com/2020/04/01/accurate-dispensing-of-toilet-paper-will-get-us-through-the-crisis/>

当我们进入与新冠肺炎相关的官方封锁的第二个星期时，很明显，我们必须节约一些资源来帮助我们度过这一切。我们不能因为可以去商店买更多的东西就把所有的东西都用完，我们必须看看我们已经有了什么，并把它当作必须让我们度过接下来的三个月。在我们偶尔去超市的时候，并不总是确定他们会有我们想要的东西。

[![This is the very last of the toilet paper in my local supermarket, on the 8th of March.](img/44823b34b507feca834c9267b50992f2.png)](https://hackaday.com/wp-content/uploads/2020/04/zx-bogroll-no-bogroll.jpg)

This is the very last of the toilet paper in my local supermarket, on the 8th of March.

卫生纸尤其短缺。新闻里充斥着人们为最后 12 包啤酒而战的镜头，自上个月初以来，无论是为了爱还是为了钱，都没有一包啤酒。为了保存库存，并使我们免于不得不将每日邮报剪成正方形并挂在墙上的绝望措施，需要一种技术解决方案。为此，我发明了一种电脑化的卫生纸卷分发器，它仔细控制着这种珍贵卫生产品的数量，希望通过抑制其消费来帮助我们度过危机。

在完全封锁的情况下，很难确保我们通常的制造商必需品立即交付，因此，与其发送我可能喜欢的控制板，还不如用我现有的东西来凑合。最后，我选择了我放在长凳下的一个盒子里的一台老式单板计算机。Sinclair ZX81 拥有一个运行频率为 3.25 MHz 的单核 Z80 处理器，双通道内存，一个 Ferranti GPU，以及黑色塑料外壳的大量扩展可能性。我选择它是因为我可以将它的[热敏打印机外设](https://en.wikipedia.org/wiki/ZX_Printer)重新用作卫生纸打印机，还因为它有一个易于擦拭和卫生的薄膜键盘，而不是传统的可能滋生细菌的键盘。

在硬件方面，我发现我能够相当容易地将一卷标准的 Cushelle 应用到 ZX 打印机上，并且很快就用下面的基本代码分发了纸张。

```

10 REM TOILET PAPER PRINTER
20 FOR T=0 TO 44
30 LPRINT ""
40 NEXT T
50 LPRINT "---------- TEAR HERE -----------"

```

现在它在长凳上工作，但很快它就会被安装在厕所旁边的墙上，作为一个小型便携式电视的监视器。分发卫生纸将像输入`RUN`和点击 ZX 的新线路键一样简单，然后看着一张卫生纸神奇地从打印机中出现。像这样的小窍门将会对我们度过危机非常有用。毕竟，这个辛克莱总是有一块多余的地方。