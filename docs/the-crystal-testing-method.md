# 晶体(测试)法

> 原文：<https://hackaday.com/2018/10/20/the-crystal-testing-method/>

过去，任何优秀的电子实验者都有一个装满晶体的袋子，因为你永远不知道你可能需要什么频率。现在，你很可能拥有更少的频率，因为你通常只需要一个参考频率，并从中获得所有其他频率。但是你如何测试一个水晶呢？正如【穆萨】在[最近的一个视频](https://www.youtube.com/watch?v=hE1VPbXW_Bc)中指出的，你不能用万用表测试它。

他的方法很简单:用示波器监控一个函数发生器，但将晶体串联起来测试。然后移动频率，直到看到示波器上的电压峰值。这个频率应该和晶体的工作频率相匹配。

有趣的是，由于晶体的谐振，示波器上的电压可以比信号发生器的输入电压高得多。这是一个简单但有效的测试。当然，你也可以用一个小振荡器，看看晶体在实际电路中的表现。

我们之前已经用网络分析仪测试过晶体，我们甚至制作了一个视频，展示了与 Mousa 基本相同的测试，尽管是在 LC 电路上，而不是在晶体上。你需要小心，不要让晶体意外地工作在泛音模式，尽管假设它工作在谐波上，它也应该工作在基频上。我们还看到了用[软件定义无线电](https://hackaday.com/2018/06/06/classifying-crystals-with-an-sdr-dongle/)完成的晶体测试和分类。

 [https://www.youtube.com/embed/hE1VPbXW_Bc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/hE1VPbXW_Bc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

