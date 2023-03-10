# 使用激光切割机复制光学比较仪屏幕

> 原文：<https://hackaday.com/2022/05/30/using-a-laser-cutter-to-replicate-an-optical-comparator-screen/>

精密仪器通常包含对其功能至关重要的专用组件，但如果出现故障，几乎不可能更换。[Andre]在光学比较仪方面就遇到了这样的问题，光学比较仪是一种通常在机械车间使用的仪器，用于帮助检查成品零件的公差。它是通过将一个物体的放大图片投射到一个玻璃屏幕上，屏幕上有显示角度和距离的标记。

在易贝买的老式比较仪中，玻璃上的标记已经褪色到几乎无法使用的程度。因此，他联系了 Clough42 的[James]，他能够使用激光切割机制作出近乎完美的替代屏幕，如下面嵌入的视频所示。

第一步是在 CAD 程序中复制屏幕上的标记。[James]解释了 Fusion 360 中的过程，演示了如何通过适当使用约束、变量和模式来几乎自动生成所有不同的比例。然后，他将图纸转移到 Lightburn，后者驱动激光切割机，将标记蚀刻到一片覆盖有 CerMark 的玻璃上，CerMark 是一种标记溶液，当被激光加热时会变成深黑色。

蚀刻后，最后一步是在玻璃上涂上磨砂，把它变成一个投影屏幕。虽然有几种方法可以实现这一点，但[James]选择了一种简单的基于喷雾的方法，它给出了令人惊讶的好结果。经过几次实验，我们发现在玻璃背面蚀刻标记，并在那一面涂上磨砂，可以获得清晰度和耐用性的最佳组合。

[詹姆斯]的项目表明，如果你有合适的工具，即使是带有定制玻璃组件的精密仪器也可以修复。类似的策略可能也适用于为模拟仪表，甚至是旧的收音机刻度盘创建自定义刻度。如果你不熟悉激光切割机，看看我们用 Ortur 型号做的实验[。谢谢你的提示，波伊特！](https://hackaday.com/2021/02/23/hands-on-with-the-ortur-laser-cutter/)

 [https://www.youtube.com/embed/hJJnBxhGnWY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/hJJnBxhGnWY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

