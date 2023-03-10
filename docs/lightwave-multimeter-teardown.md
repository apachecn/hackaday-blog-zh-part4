# 光波万用表拆卸

> 原文：<https://hackaday.com/2021/07/06/lightwave-multimeter-teardown/>

你倾向于用相当基本的术语来考虑测试设备:万用表、电源、信号发生器和示波器。然而，有大量高度专业化的测试设备用于非常特殊的目的。其中一个是 8163A“光波万用表”，[信号路径]在最近的一个视频中撕裂了一部分用于[维修](https://www.youtube.com/watch?v=ZLeZcbf_E0A)，你可以在下面看到。

如果你从未听说过光波万用表，不要难过。该仪器是一个光纤测量系统，根据安装的插件，可以管理一些通常使用光功率计、激光或光源以及一些专用测试夹具来执行的测试。

这些仪表价格昂贵，甚至是二手的，所以[信号路径]挑选了一个不起作用的。如果你能修理一个仪器，这是一个低成本建立一个严肃的测试平台的好方法。当然也有风险，就是找不到问题所在或者找不到合适的更换零件。但是这种旧测试设备的问题通常很简单。在这种情况下，盒子通电了，但是除了闪烁的 LCD 屏幕之外什么也没有。

该设备很难接近，但随着主板的拆除，它显示了一个 x86 处理器和一个装满组件的大电路板。甚至还有一个 FPGA。许多元件没有组装，因此同一电路板可能还具有其它功能。

这种情况并不常见，但我们都有过神秘地拆开某样东西让它工作的时候，这次就是其中之一。我们的怀疑是，取出电缆，并把它们放回主板和前面板之间恢复的连接。但是谁知道呢？

大约 8 分钟后，你可以很好地了解该设备是如何工作的，并拆除一些插件模块。这是那种你可能永远都不需要的测试装备，看看它的内部和外部是如何工作的是很有趣的。

令人惊讶的是有这么多特殊的测试设备。我们最喜欢的是来自 B & K 的电视分析师。一些与太空有关的[旧装备](https://hackaday.com/2021/06/19/apollo-shift-register-is-discrete/)也很有趣。

 [https://www.youtube.com/embed/ZLeZcbf_E0A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ZLeZcbf_E0A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

