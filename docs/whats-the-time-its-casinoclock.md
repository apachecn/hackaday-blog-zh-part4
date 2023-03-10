# 几点了？赌场的钟到了！

> 原文：<https://hackaday.com/2022/07/30/whats-the-time-its-casinoclock/>

俗话说，没有什么是确定的，除了死亡、税收和黑客永无止境的创造力。不管一个概念是如何被尝试和证明的，总会有人为它找到一个新的转折。例证:臭名昭著的时钟制造者【Shinsaku Hiura】采用了古老的分瓣显示方法[，并通过使用一副扑克牌来混合显示时间](https://www.instructables.com/Casinoclock/)。

从技术上来说，这种时钟的工作原理就像一个普通的翻盖时钟，只是翻盖的上半部分用于显示数字，而下半部分则显示卡片的背面。除此之外，机械结构是相同的:一组固定卡片的铰链排列在一个由步进电机驱动的转子上，直到显示正确的数字为止(Thingiverse 上有 [STLs)。a 低，小丑是零，皇后在中午罢工。](https://www.thingiverse.com/thing:5234371/files)

它的中心是一个 ESP32，控制每个数字的电机驱动器，并通过 WiFi 检索时间，使一般组件数量方便地保持在较低水平。当然，一种选择是按照卡片的顺序排列卡片，以使旋转保持在最低限度，但让我们现实一点，拍打的声音是这里一半的乐趣。因此，[Shinsaku Hiura]随机排列卡片，并将其映射到相应的代码中。休息之后，您可以在视频中看到所有的操作，以及一些额外的设计信息。

对于他的更多时钟创作，请查看[这种不同的翻转时钟方法](https://hackaday.com/2021/11/24/a-flip-clock-that-flips-up-not-down/)和[空心时钟](https://hackaday.com/2022/01/08/hidden-shaft-and-gears-make-this-hollow-clock-go/)。但是如果你对未来比对现在更感兴趣，[这里有一副配套的塔罗牌](https://hackaday.com/2020/05/29/tarot-machine-flips-through-fates-rolodex/)。

 [https://www.youtube.com/embed/GRZh4gPptd4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/GRZh4gPptd4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

