# 硬币接收器比你想象的更高科技

> 原文：<https://hackaday.com/2022/04/10/coin-acceptors-are-higher-tech-than-you-think/>

投币机的历史比你想象的要长。例如，古代寺庙用它们向信徒分发圣水以换取他们的硬币。当你投入一枚硬币时，老式投币电话会发出铃声，这样接线员就知道你付钱了。旧的弹球机有一根线来抓住中间有洞的东西，所以你不能玩垫圈。但是像其他事情一样，硬币接受者已经进步了不少。[Electronoobs] [展示了一个可以接受不同国家硬币的单元](https://electronoobs.com/eng_arduino_tut169.php)而且里面出奇的复杂。他用他从拆卸中学到的东西构建了自己的基于 Arduino 的版本。

为了扩大规模，香蕉是必不可少的。盒子里有几个感应线圈和一些光电设备。特别是，有两个光学传感器可以观察硬币滚下斜坡。这产生了两个脉冲。脉冲的宽度表示硬币的直径，脉冲之间的时间告诉它的速度。

[![](img/8315beff6c9be59b29b8407823f24d95.png)](https://hackaday.com/wp-content/uploads/2022/04/coin-acceptor-inner.jpg) 那么这两个线圈是干什么用的呢？它们形成一个变压器，线圈之间移动的硬币以一种取决于材料的方式改变耦合。通过了解硬币的直径、通过速度和材料，你可以识别硬币。一个小小的螺线管驱动的翻板移开来存放一枚被识别的硬币。如果它不移开，硬币就会从投币口出来。

我们想知道机器是如何知道当地货币的，以及如果硬币的成分发生变化会发生什么。该视频显示了如何通过多次插入硬币样本并让设备进行测量来教授设备关于硬币的知识。因此，即使您有一些自定义令牌，它也应该工作。

自制解决方案非常简单，尤其是光学部分。线圈的工作有点多，因为你需要一个大线圈以及相关的驱动器和传感电子设备。然后，当然，还有机械，他没有建立，因为商业产品只有 20 美元。

我们总是喜欢拆卸，但这一次是特别有益的，我们喜欢操作原理的复制。希罗是生活在很久以前的希腊人，他一定会对这次拆卸很感兴趣。我们不禁也想到了【彼得的】[投币计算器](https://hackaday.com/tag/coin-operated/)。

 [https://www.youtube.com/embed/Kl7uTviiOG0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Kl7uTviiOG0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

