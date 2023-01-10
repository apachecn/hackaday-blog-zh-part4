# 微波倍频器

> 原文：<https://hackaday.com/2021/10/18/a-microwave-frequency-doubler/>

这是一个古老的问题。你有一个 2.5 GHz 的信号源，你想用 5 GHz。你需要一个倍频器。[全电子频道]有一个有趣的视频，不仅讲述了这种设备的理论，还展示了一个用空白 PCB 基板上的铜条制成的实用设备。

微波的一个有趣之处在于，即使是很小的铜条也是电路元件，因为 2.5 GHz 的波长只有 12 厘米。这意味着四分之一波长的短截线只有 3 厘米，刚刚超过一英寸。

所用的构建技术很简单，正如他指出的那样，用真实电路做实验会让你对这些电路的工作原理有更多的感受，而不仅仅是阅读和计算。

乘法器驱动放大器进入非线性状态，这当然会产生谐波。然后带通滤波器选择二次谐波。如果你以前没有处理过短线电路，你可能想[阅读一下](https://en.wikipedia.org/wiki/Stub_(electronics))关于一端连接的铜片如何像电感、电容甚至调谐电路一样工作。

如果你想要更多关于铜带技术的细节，[我们可以帮助](https://hackaday.com/2017/07/25/rapidly-prototyping-rf-filters/)。如果你不想倍频，也许你会更喜欢[试电压](https://hackaday.com/2017/03/22/how-does-a-voltage-multiplier-work/)。

 [https://www.youtube.com/embed/XPMRzLGf4SI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/XPMRzLGf4SI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

