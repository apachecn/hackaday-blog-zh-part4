# 拆开脉冲变压器开关

> 原文：<https://hackaday.com/2019/06/03/tearing-apart-pulse-transformer-switches/>

如果你喜欢机械键盘，你就喜欢开关。从历史上看，开关很奇怪，Topre 电路板上有奇怪的电容橡胶圆顶开关，IBM M 型有弯曲弹簧，早期 IBM 键盘上有梁弹簧。[惠普信号发生器的拆卸有史以来最奇怪的键盘开关](https://www.youtube.com/watch?v=cA2tTNO23x0)。它们被称为脉冲变压器开关，但它们是我们见过的最奇怪、最古怪、最复杂的键盘开关

从机械角度来说，这些按键安装在一个 1×5 的塑料框架上，框架上有一个向下压在(黄铜？)光刻版。从机械上来说，这实际上是一个金属圆顶键盘，它只是简单地将一块有弹性的金属压在印刷电路板上的一个触点上。这是机械上的解释，电气操作理论要奇怪得多。

从电学角度来看，这种键盘由一个印刷电路板组成，每个按键下有两个线圈。该电路是有线的，因此两个键可以用多路复用器的脉冲同时“读取”。该脉冲在两个单独钥匙的“感应”线圈中感应出电流，该电流被发送到比较器。如果两个键都没有按下，比较器会看到一个正电压和一个负电压相互抵消，这意味着没有键被按下。如果按下一个键，金属圆顶会使键盘下方的变压器短路，这意味着比较器只能看到一个电压，该键被记录为被按下。

这是一些疯狂的键盘电路，我不会轻易这样说。有“声学”键盘，它由一排敲击金属棒的键组成，金属棒两端各有一个声学传感器。通过测量击键声音到达金属棒两端的时间，可以记录击键。这是怪异和昂贵的建设，但它仍然比脉冲变压器开关简单。看看下面的视频。

 [https://www.youtube.com/embed/cA2tTNO23x0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/cA2tTNO23x0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

