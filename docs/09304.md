# 激光检流计和 ESP32 重现老派小行星

> 原文：<https://hackaday.com/2021/02/18/laser-galvos-and-an-esp32-recreate-old-school-asteroids/>

现在玩*小行星*已经不是 40 年前它问世时的样子了。当时，矢量扫描显示器是魅力的一部分；对于纯粹主义者来说，用一个运行在传统光栅显示器上的仿真器来凑合并不太合适。但是如果你设法像[克里斯 G]一样制作你自己的游戏的[激光投影版本，你就接近捕捉到游戏的一些原始魔力了。](https://hackaday.io/project/177729-laser-projected-asteroids-on-the-esp32)

关于这个项目有很多东西需要解开，下面的视频很好地解释了它。最初的游戏使用阴极射线管内闪烁的电子束来追踪游戏中的每个物体，[Chris]用易贝现成的双轴检流计和 5 兆瓦的激光 LED 代替了它们。这可以在一面高达两米的墙上投射出一个游戏场，比任何版本的机器都要大得多。检流计由定制 PCB 上的运算放大器驱动器和 SPI DAC 驱动。与运行原始游戏的离散逻辑芯片和 6502 相比，[Chris]选择了 ESP32。

尽管硬件很有趣，但真正的故事在软件中。[Chris]很好地贯穿了他的设计，让大部分视频感觉像是游戏编程的大师课。他的软件是从头开始的——这里没有仿真。因此，它不能完美地再现原始游戏——没有飞碟，也没有飞船爆炸的动画(还没有)——但当与激光矢量显示结合时，它肯定能捕捉到原始的感觉。

作为过去的小行星迷，这个真的让我们很激动。我们之前已经看过《T2》基于激光的游戏《T3 》,但这一次让我们认为我们终于有能力夺回我们虚度的青春。

 [https://www.youtube.com/embed/LXDwGygCokU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/LXDwGygCokU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

