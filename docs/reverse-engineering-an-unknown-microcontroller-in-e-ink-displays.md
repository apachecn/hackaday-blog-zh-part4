# 对电子墨水显示器中的未知微控制器进行逆向工程

> 原文：<https://hackaday.com/2021/05/15/reverse-engineering-an-unknown-microcontroller-in-e-ink-displays/>

对于刷新率不是特别重要的单色显示器，几乎没有比 E Ink 显示器更好的选择了。它们有多种尺寸和不同的价格，但几乎没有比重新利用大规模生产和广泛使用的东西更便宜的选择，如电子墨水(有时也称为 E Ink 或 ePaper)价格标签。[至少，一旦所有的逆向工程完成](http://dmitry.gr/?r=05.Projects&proj=30.%20Reverse%20Engineering%20an%20Unknown%20Microcontroller)。

[Dmitry Grinberg]已经完成了大量不同的电子墨水模块，在他的过程中解开了它们的秘密。在这种情况下，他开始在这里展示的小型廉价显示器上对未知的微控制器进行逆向工程。最初的研究显示了 ZBS24x 系列的一个不起眼的芯片，与 SSD1623L2 E Ink 控制器封装在一起。从那里，他能够焊接到通信线，并开始通过 ISP 与设备通话。

这一努力令人印象深刻地深入到微控制器的世界，从探测各种寄存器到逐个解锁特性。它运行的是 8051 内核，所以[Dmitry]提供了一些背景知识来帮助我们了解，尽管完全控制系统仍然是一个非常令人印象深刻的艰难过程。

如果你手头正好有一个这样的价格标签，那它就是一个重新编程的无价资源，但总的来说，它也是一本很好的读物。另一方面，如果你对各种显示器的逆向工程更感兴趣，可以看看这个横跨 50 年显示技术的[艺术装置。](https://hackaday.com/2021/05/09/artwork-spans-fifty-years-of-display-technology/)