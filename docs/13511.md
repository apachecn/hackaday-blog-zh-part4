# 用这个小计时器追踪那些剩菜

> 原文：<https://hackaday.com/2022/05/01/track-those-leftovers-with-this-little-timer/>

我们都曾在生命中的某个时刻打开冰箱门，然后立刻希望自己没有打开。当我们发现上周六的剩菜已经被遗忘，并且已经变质时，一股恶臭的瘴气笼罩着我们。要是我们有办法跟踪这些事情，避免这种充满恶臭的时刻就好了。向前一步【ThinkLearnDo】，[用一个专门为此目的设计的小计时器](https://hackaday.io/project/185113-fridge-leftover-monitor)。

操作非常简单，按下按钮，将装置放在盛有剩菜的容器上。如果你在一周内没有吃完剩菜，LED 就会开始闪烁。眨眼是一个微妙的提醒，提醒我们在食物变质之前处理掉它。

板载是一个 Holtek HT68F001 微控制器，用硬币电池供电，不需要太多其他东西。Holtek 是一个不寻常的选择，它是我们比 ATmegas 和 STM32s 更少见到的几个超级便宜的中国微控制器品牌之一。这正是这样一台最小的计算机最适合的地方:一种给一个非常便宜的项目增加一点智能的方式，同时对 BoM 的压力最小。

如果你对这些芯片感兴趣，前一段时间[我们讨论了不同系列的芯片](https://hackaday.com/2019/08/28/everything-you-want-to-know-about-the-cheapest-processors-available/)，包括 Holtek 和著名的 3 分红木芯片。