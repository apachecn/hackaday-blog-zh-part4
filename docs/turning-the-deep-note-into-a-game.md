# 把深沉的音符变成游戏

> 原文：<https://hackaday.com/2018/10/21/turning-the-deep-note-into-a-game/>

最著名的电脑合成音乐作品之一是 Deep Note，这是 THX 的音频商标。它以十几个声音开始，随机调整在 200 到 400 赫兹之间，然后滑音扩展到三个八度音阶。通过几千瓦的扬声器系统，在*绝地*前播放，观众会听到。

最初的 THX 深音符是在运行 20，000 行代码的价值数十万美元的硬件上创建的，但那是在 1983 年。现在我们有了便宜的微控制器，所以，当然，你现在可以把笔记本放进你的口袋了。你甚至可以把它变成一个游戏。这正是[Bob] [用他的 Deep Synth](https://hackaday.io/project/161481-deep-synth) 所做的。这是深沉的音符，以游戏男孩的方式。

这种构建的硬件是 [1Bitsy 1UP](https://hackaday.io/project/25632-1bitsy-1up) ，这是一款复古风格的掌上游戏机，来自[Bob]的朋友[Pitor]。1Bitsy 的板载是 STM32 F4，运行频率为 168 MHz，配有 2.8 英寸液晶显示器、SD 读卡器和传统的 Game Boy 控制方案。所有的游戏都取决于你。

[Bob]为 1UP 编写了一个音频驱动程序，但需要一个好的音频演示。既然 Deep Note 对于卢卡斯影业来说是一个足够好的演示，那么它对于微控制器来说显然也是一个足够好的演示。在远远不到 20，000 行代码中，[Bob]制作了 1UP 复音，并且它惊人地快，足以合成大约 30 个振荡器。实际上它听起来也像是高音。休息过后，你可以看看视频(和音频)。

 [https://www.youtube.com/embed/wK5Sz6IzRqE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/wK5Sz6IzRqE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

