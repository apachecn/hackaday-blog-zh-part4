# 固态继电器模拟，解释

> 原文：<https://hackaday.com/2020/02/19/solid-state-relay-simulation/>

[SaltyPuglord]需要一个固态继电器用于一个项目。我们刚刚买了一个，但是他决定在 LTSpice 设计他自己的。在这一过程中，他制作了下面的视频，内容丰富，是 LTSpice 中非平凡设计的一个很好的例子。

MOSFETs 使这种设计变得更加简单，就像将一对结实的 fet 与交流电源和负载串联起来一样简单。然而，这有几个分支[咸]涵盖在视频中。

最大的担忧来自于将 DC 的供应与地面隔离。他使用了一个很难在 LTSpice 中模拟的变压器。除此之外，电源的设计非常简单，正如他在视频中提到的，你真的不需要这么复杂的稳压器来为 MOSFETs 的栅极供电。

另一个问题是，两个 MOSFETS 之间的导线必须悬空，并且能够处理相当大的电流。问题是，如果 fet 没有接地参考，LTSpice 可能会变得混乱。因此，模拟电路中存在接地。其实默认的 LTSpice 求解器反正不喜欢电路。该视频展示了如何切换到运行良好的替代解算器。

看起来视频中谈论的很多内容在 TI 的一份链接文件[中也有提及。如果你想在不安装 LTSpice 的情况下尝试一个轻型版本的电路，请尝试](https://www.ti.com/lit/ug/tiduc87a/tiduc87a.pdf)[法尔斯塔德](http://tinyurl.com/qrzwnlr)。如果你想安装不同的东西，可以试试[微型瓶盖](https://hackaday.com/2020/01/08/commercial-circuit-simulator-goes-free/)。如果你坚持使用 LTSpice，并且你想[学习更多关于建模变形金刚](https://hackaday.com/2016/03/02/transforming-spice/)的知识，我们会帮你搞定。

 [https://www.youtube.com/embed/1-De7jaC-R8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/1-De7jaC-R8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/1-De7jaC-R8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/1-De7jaC-R8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

