# 避免 PCB 串扰

> 原文：<https://hackaday.com/2021/01/25/avoiding-pcb-crosstalk/>

既然制造 PCB 相对便宜且容易，那么在项目中使用 PCB 就成了家常便饭。然而，创建高性能电路板有许多微妙之处，在您的 555 LED 闪光灯上不会显示太多。[Robert Feranec]精通电路板布局，最近他与 Teledyne LeCroy 的[Eric Bogatin]一起制作了一部关于信号串扰的动画。如果你想很好地理解相声以及如何与之斗争，你会想看看下面视频中[Eric 的]介绍。

简而言之，问题的核心在于让轨迹靠得很近，这样一条轨迹的磁场就会与另一条相交。数学是令人毛骨悚然的，但[Eric]谈到了系统建模的简单方法，这些方法可能不精确，但对于实际设计来说足够接近。

这些模型使用电感和电容来表示不同模式的串扰，您可能已经知道如何处理这些量。该视频展示了一些模拟，并提出了控制问题的方法。

尽管主题是 PC 板，但一些相同的想法也适用于电缆。例如，出于类似的原因，以太网电缆也有 FEXT 规格。

我们自己的[Bil Herd]有一个你可能会喜欢的类似话题。[费拉内克]是[联邦学院的幕后推手，我们之前已经读过关于它的评论](https://hackaday.com/2017/05/09/learn-advanced-pcb-design-for-200-worth-it/)。

 [https://www.youtube.com/embed/EF7SxgcDfCo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/EF7SxgcDfCo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

