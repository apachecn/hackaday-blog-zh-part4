# 比较两款 Game Boy 音频芯片上的裸硅

> 原文：<https://hackaday.com/2020/06/27/comparing-bare-silicon-on-two-game-boy-audio-chips/>

我们总是期待着一篇由[Ken Shirriff]撰写的新博文，而最新的这篇并没有让我们如愿以偿。他这次的话题？[对比两款 Game Boy 音频芯片](http://www.righto.com/2020/06/reverse-engineering-and-comparing-two.html)。人们之前已经注意到，游戏男孩颜色听起来与经典游戏男孩非常不同，他想找出原因。如果你了解他的工作，你不会惊讶地发现这种比较包括将芯片从 IC 封装中剥离出来。

[Ken]用显微照片很好地解释了晶体管、电阻和电容在芯片上的出现方式。他指出，众所周知，电阻器很难在生产 IC 上精确制造。许多差异会影响绝对值，因此设计人员尽量不要指望精确的值，或者，如果他们指望精确的值，就求助于激光调整或其他技巧。

然而，电容器是不同的。电容的准确值可能很难预先猜测，但同一芯片上两个或更多电容值的比值将非常精确。这是因为电介质——芯片的氧化层——会非常均匀，而且照相过程可以非常精确地控制电容器极板的平面面积。

我们之前已经对芯片进行了解封装，我们不得不说，如果你刚刚开始在芯片层面上看待芯片，这些带有双极晶体管的大芯片比你甚至在 20 世纪 80 年代的 CPU 中找到的精细和密集的几何结构更容易处理。

我们总是喜欢与[Ken]联系。有时他会拆卸核导弹。有时他在[修理一台旧电脑](https://hackaday.com/2018/09/20/fixing-an-ibm-1401-computer-to-get-it-printing-again/)。但它总是很有趣。