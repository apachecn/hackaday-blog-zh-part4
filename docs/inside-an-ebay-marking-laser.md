# 在易趣激光打标机里

> 原文：<https://hackaday.com/2022/06/11/inside-an-ebay-marking-laser/>

说到在易贝寻找酷的东西，有些人运气很好。虽然我们似乎遇到的都是假冒芯片和明显损坏的设备，列为“状况良好，电源开启”，但[Les Wright]实际上通过他最近在易贝购买的一辆车[获得了比他期望的更多的东西。](https://www.youtube.com/watch?v=_i1J7TGpPnQ)

在他拆卸和参观一台工业打标激光器的视频中，[Les]暗示他真的只是为了光学而参与其中——这并不奇怪，因为他对一般的[光学](https://hackaday.com/2021/04/23/pi-based-spectrometer-puts-the-complexity-in-the-software/)和特别的[激光器](https://hackaday.com/2021/08/09/using-a-laser-to-blast-away-a-bayer-array/)感兴趣。20 瓦的 CO [2] 激光器曾经在装配线上将条形码之类的东西蚀刻到产品上，但是它有自己的 2009 年的日期代码，这是一个安全的赌注，它是由于烧坏的激光管而定的。但仍有高质量的红外光学器件和精密的 X-Y 检流计组件有待收获，所以[Les]继续努力。

激光器本身最终是围绕着一个 Synrad 射频激励的 CO [2] 管建造的。幸运的是，[Les]发现激光器实际上仍然工作，至少在大部分时间里。射频驱动器似乎出现了间歇性问题，但激光工作的时间足够长，可以从任何阻挡它的可燃物中释放出神奇的烟雾。galvos 也可以——[ Les]可以用一个 Teensy 和几个开源库来驱动它们。

Galvos，价值超过 800 美元的镜头，和一个正常工作的激光管——还不错。我们将继续跟踪，看看[莱斯]如何看待这些战利品。

 [https://www.youtube.com/embed/_i1J7TGpPnQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/_i1J7TGpPnQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

