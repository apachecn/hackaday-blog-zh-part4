# 无线发光二极管其实并不神奇

> 原文：<https://hackaday.com/2021/11/29/wireless-leds-arent-really-magic/>

[Atomic14]购买了一些从基站接收电能的无线 led。它们包装得非常整齐，但是——我们喜欢——他把其中一个拆开，做了自己的版本。它们可能看起来不那么精致，但它们确实有用，而且不可否认它们很酷。

led 通过从感应线圈接收电能来工作。一旦你有了电，点亮一个 LED 就没什么大不了了。逆向工程发现，发射机发送 217 千赫到 2.2 兆赫兹电感。一个电容使线圈谐振，并驱动相连的 LED。

一些实验发现，该电路可以提供大约 2 mA -3 mA 的电流。[Atomic14]使用两个发光二极管来完成交流波形的每一半。他还解剖了发射器，所以你也可以在那里滚动你自己的。

你会用无线 LED 做什么？也许是模型展示或棋盘上的灯光？我们想知道您是否可以使用两种或更多种电源频率来发出信号(例如，200 kHz 点亮红色 LED，而 250 kHz 点亮绿色 LED)？最初的发射器是固定频率的，但如果使用微控制器，就很容易使其频率捷变。最后，有一个经济分析是关于建造这些还是购买现成的，但是我们都知道这并不总是一个严格基于美元的决定。商业版本看起来确实更好一点，但对于表面贴装元件，即使是 DIY 版本也可能看起来更干净一点。

事实上，我们以前已经见过这些 T1。我们想知道你是否能[从某种正在传输的东西中获取能量](https://hackaday.com/2021/10/19/sign-detects-rf-to-show-you-are-on-the-air/)。

 [https://www.youtube.com/embed/jdc_0r5pJPc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/jdc_0r5pJPc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

