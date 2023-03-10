# 动态雕塑通过机器学习实现平衡

> 原文：<https://hackaday.com/2018/10/26/kinetic-sculpture-achieves-balance-through-machine-learning/>

我们都知道实现生活平衡有多重要，至少自助行业是这么告诉我们的。然而，如何准确地达到平衡通常是留给个人的练习，结果各不相同。但是我们的机器呢？会不会有一天，人工智能和它们的机器人身体变得如此紧张，以至于它们也会寻找一种难以捉摸和难以定义的平衡感？

我们开玩笑，但只是一点点；谁知道机器心理学的未来领域会发现什么？在那之前，[这个实现文字平衡的动态雕塑](http://astridkraniger.com/InMedioStatVirtus.html)可能对人类和机器都有借鉴意义。在 Medio Stat 维尔图斯杂志中被称为*或“站在中间的美德”【Astrid Kraniger】的动态雕塑探索了一个简单的系统如何通过机器学习找到稳定的平衡。这个任务看起来很简单:让一个球保持在一条轨道的中心，轨道由两根缆绳悬挂着。电缆的长度由步进电机改变，而球的位置通过两根电缆之间的重量差来检测，使用的是从行李秤收集的测压元件。马达升高和降低每一面，以平衡每一面上的力，最终达到平衡。*

这里的转折是，[Astrid]选择使用 Q-Behave 库将机器学习应用于该问题，而不是简单的 PID 循环或另一种控制算法。系统检测两个权重之间的差异何时减小，并“奖励”算法，以便它了解对它的要求。结果是一个系统平稳地进入平衡状态。看看下面的视频；这是一种奇怪的安慰。

我们以前见过自平衡系统，从[滚珠平衡 Stewart 平台](https://hackaday.com/2014/08/22/stewart-platform-ball-bearing-balancer/)到[类似赛格威的两轮平衡器](https://hackaday.com/2012/07/20/self-balancing-robot-uses-cascading-pid-algorithms/)。人们想知道机器学习是否也可以应用于这些系统。

[https://player.vimeo.com/video/295565389](https://player.vimeo.com/video/295565389)