# 双线对讲机的逆向工程

> 原文：<https://hackaday.com/2019/10/27/reverse-engineering-a-two-wire-intercom/>

曾经有一段时间，对讲机只是一对盒子，里面有几根电线连接着扬声器，还有一个音频放大器。但是对讲机已经像其他所有东西一样加入了数字时代，所以这两条线现在承载了数字信号的其他功能。[Aaron Christophel]以安装这些设备为生，并发布了一个有趣的逆向工程视频，我们也将它放在了 break 的下方。

该系统的电源是恒定的 24V DC，音频仍然是我们都熟悉的老式模拟信号。然而，在 24V DC 上施加了一系列脉冲序列来触发不同的警报和其他功能，他描述了在向我们展示他用来通过 Arduino 发送和接收脉冲的电路之前，用示波器提取这些脉冲。视频的大部分是关于 Arduino 上的软件，你也可以在 GitHub 库中找到[。](https://github.com/atc1441/TCSintercomArduino)

对于那些喜欢系列侦探工作的人来说，这是一本有趣的入门书，即使他们手头没有对讲机。

 [https://www.youtube.com/embed/xFLoauqj9yA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/xFLoauqj9yA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

