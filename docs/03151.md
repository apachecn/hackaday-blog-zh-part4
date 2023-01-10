# pandaptors 并不是从 SDR 开始的

> 原文：<https://hackaday.com/2019/06/08/panadaptors-didnt-start-with-sdrs/>

现代全唱全舞业余无线电收发机上的必备附件是一个 panadaptor。不可避免地受到 SDR 技术的驱动，它是频域中一个频带的视图，通常会显示为“瀑布”,提供一个时间维度来查看一段时间内的传输情况。

[Bill Meara，N2CQR]提醒我们，panadaptors 并不是什么新东西，事实上，它们可以追溯到上个世纪上半叶，甚至不需要 SDR 就可以工作。为了证明这一点，[他为 40 米业余乐队](https://soldersmoke.blogspot.com/2019/05/diy-waterfall-quick-and-easy-panadaptor.html)制作了一个。

模拟 panadaptor 背后的原理非常简单，它是一个普通的接收器，其本地振荡器在所需频带上进行线性周期扫描，其输出驱动示波器的 Y 轴，示波器的 X 轴由扫描驱动。在[Bill]的例子中，接收器是 BitX 自制收发器，扫频本地振荡器由他的 Foeltech 信号发生器提供。通过触发扫描范围底部的标记频率来同步示波器。他制作了一个视频来展示这一过程，你可以在视频的下方看到。

制造这种简单的频谱分析仪有很多途径，事实上我们中的一些人已经用电视调谐器尝试过 ti。

 [https://www.youtube.com/embed/uqYXIU9G6iM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/uqYXIU9G6iM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

