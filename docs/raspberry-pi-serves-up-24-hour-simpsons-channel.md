# 树莓派提供 24 小时辛普森频道

> 原文：<https://hackaday.com/2020/02/07/raspberry-pi-serves-up-24-hour-simpsons-channel/>

免费视频点播是每个电视迷几十年来的梦想，现在我们终于实现了。但是怀旧有一种有趣的方式让一些人怀念过去的日子，即使我们知道这在技术上是一种倒退。想要重现 1998 年左右的电视观看体验，[【普罗布诺】想出了一个运营自己的电视频道](https://www.youtube.com/watch?v=CtPHZ5pG6nA)的方法。

有了树莓派和数字调制器，他就有了这个街区唯一一栋全天播放《辛普森一家》的房子。他完全不能控制下一集播放哪一集，他不能暂停它，它以标准清晰度呈现(这对任何在网飞时代长大的人来说都是一场噩梦)，但对我们其他人来说却是一种熟悉的观看体验。

[![](img/39252cd2042eae5300392a38ca5d4dc8.png)](https://hackaday.com/wp-content/uploads/2020/02/pitv_detail.jpg)

Where we’re going, we don’t need HDMI.

这个项目的关键是通道加 3025 型调制器。它从天线接收信号，并在用户定义的频道上混合两个复合视频源。所有[普罗布诺]要做的就是找到一个不会干扰任何无线电台的频道。调制器已经接入了房子的同轴电缆，因此任何连接到墙上的电视都可以参与进来。不需要特殊设置:当他想看《辛普森一家》时，他只需将最近的电视调到合适的频道。

为调制器提供视频的是 Raspberry Pi，具体来说，是具有复合视频输出功能的原始模型。虽然目前第一代 Pi 有点老了，但播放标清视频肯定在其能力范围内。有了一个装有几百集节目的 u 盘和一点脚本，它就能直接从斯普林菲尔德传送永无止境的视频流。调制器上还有第二个通道可用，我们认为它可能非常适合《宋飞正传》或《X 档案》中的 T2。

有趣的是，这不是我们第一次看到树莓派被用来提供源源不断的《辛普森一家》。但是与[之前必须直接连接到电视](https://hackaday.com/2016/05/08/rasberry-pi-zero-plays-every-simpsons-episode-ever-at-random/)的尝试相比，我们喜欢使用调制器和创造更真实体验的想法。

 [https://www.youtube.com/embed/CtPHZ5pG6nA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/CtPHZ5pG6nA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

