# 通过切换以太网速度缓慢泄漏数据

> 原文：<https://hackaday.com/2020/11/30/leaking-data-slowly-by-switching-ethernet-speeds/>

气隙指的是在没有连接到外部网络的情况下运行一台或多台机器。从字面上看，在机器和外界之间存在一个空气间隙。这些措施对那些希望从这种机器中获取数据的人来说是一个挑战，导致了一些创造性的黑客行为。[【亚采克】最近一直在试验通过以太网适配器泄露数据。](https://lipkowski.com/etherify4/)

该黑客建立在[亚采克]早期的树莓 Pi 4 工作基础上，其中板载适配器在 10 兆和 100 兆模式之间快速切换[，以创建一个可以通过无线电接收到 100 米远的信号](https://hackaday.com/2020/11/09/ethernet-goes-to-the-ether/)。从那时起，【亚采克】确定树莓 Pi 4，[或者至少是他特别的一个](https://lipkowski.com/etherify3/)，似乎从以太网端口非常泄漏射频能量。他决定更深入地研究，在其他硬件上尝试同样的技术。

[使用一对通过以太网电缆](https://lipkowski.com/etherify4/)背靠背连接的戴尔笔记本电脑，采用了相同的速度切换技巧。然而，大多数硬件比 Pi 4 需要更长的时间来切换速度；通常在 2-5 秒的数量级。这限制了信号传输的速度，但是[亚采克]能够使用 QRSS，也就是众所周知的慢速莫尔斯电码，来设置这种传输数据。最好的结果是接收到 10 米外的信号，尽管[亚采克]怀疑这可以通过更好的天线硬件来改善。

虽然这种通信的低数据速率和单向性质限制了这种攻击的效用，但它表明保护机器并不像从网络上拔掉插头那么简单。对于那些有兴趣了解更多信息的人来说，我们以前做过一个关于这类黑客的专题。休息后的视频。

 [https://www.youtube.com/embed/je8fuDXTyz8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/je8fuDXTyz8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

