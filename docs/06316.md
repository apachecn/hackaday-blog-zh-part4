# 测试未知的保险丝，但不要破坏它们

> 原文：<https://hackaday.com/2020/04/20/test-unknown-fuses-without-destroying-them/>

保险丝有问题。从表面上看，测试似乎是一次性的——超过额定电流，看看它是否会爆炸。但是一旦你知道了答案，这个装置就没用了。要是有一种不损坏保险丝的方法就好了。

事实证明是有的，而且[Kerry Wong]编了一个关于他尝试非破坏性测试引信的故事。问题中的保险丝并不花哨——只是标准的玻璃管型，来自亚马逊上的廉价分类套件。问题就在这里:这样便宜的设备可信吗？要找到答案，需要比许多人更深入地钻研保险丝技术，包括了解保险丝元件的热和电特性。

[Kerry]的测试设置很简单，由一个恒流电源和一个跨接在保险丝两端的电压表组成，用来测量保险丝元件电阻引起的电压降。随着电流的增加，电压降线性增加，因为合金的电阻随着温度的增加而增加。这只能持续到保险丝电阻开始呈指数增长的时候。超过电阻翻倍的点会烧断保险丝，所以这是他测试的终点。也许不出所料，他的无名保险丝都大大超过了额定电流，证明你得到了你所付出的。有关测试和结果分析，请参见下面的视频。

知道有一种方法可以检查保险丝而不使其爆裂是很方便的，我们将把这一条存档以备将来参考。不要忘记，在排除故障时，你应该经常检查保险丝，因为你永远不知道最后一个人对它做了什么。

 [https://www.youtube.com/embed/RaSp_lY3E2U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/RaSp_lY3E2U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

