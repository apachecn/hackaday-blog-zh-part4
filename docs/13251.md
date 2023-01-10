# ESP32:两个人比一个人好吗？

> 原文：<https://hackaday.com/2022/04/04/esp32-is-two-better-than-one/>

我们之前已经看过了 WROOM-DA 模块。这是一个有两个天线的 ESP32，安德烈亚斯·斯皮斯说这是他见过的最丑的 ESP32。但是美丽毕竟是肤浅的。安德烈亚斯在双天线中发现美了吗？看下面的视频，自己看吧。

根据框图，双天线不是同时使用，而是一次提供一个分集。还有 8GB 8mb 的闪存，是传统 WROOM 模块的两倍。安装该设备有点困难，因为大多数 ESP32 载板会阻挡天线阵列的某些部分。

深入研究软件，你可以改变模式，这样你就可以将一个天线专用于接收，另一个天线专用于发射，或者你可以让设备自己找出最佳策略。正如您经常看到的，硬件将天线称为单元 1 和 2，而软件则使用 0 和 1。

[Andreas]想知道自动模式是否工作良好，所以他设计了一个测试，要求到屋顶上比较标准模块和双天线模块。DA 单元看起来工作得更好。然而，自动模式以一种令人惊讶的方式发挥作用。测试装置在每个天线上接收到相当多的电台，但自动模式接收到的电台比任何一个天线单独接收到的电台都少。

例如，在一个方向上，模块在第一个天线上接收到 30 个电台，在第二个天线上接收到 57 个电台。但是自动模式只接收到 20 个电台。没有解释，但是视频评论有不少理论。

去年我们[看了这些模块](https://hackaday.com/2021/05/21/new-part-day-esp32-wroom-da/)。如果你需要启动你的 ESP32 冒险活动，[Andreas]有许多有用的视频。还有这些[教程](https://hackaday.com/2017/03/01/esp32-tutorials/)。

 [https://www.youtube.com/embed/F0u5qIwwY1k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/F0u5qIwwY1k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

