# 384 霓虹灯成为吸引人的展示品

> 原文：<https://hackaday.com/2020/07/23/384-neon-bulbs-become-attractive-display/>

多年来，霓虹灯激发了许多散文，其迷人的光输出受到了热烈的吹捧。[Pierre Muth]是他的超级粉丝，他决定花一年时间为他的办公桌设计一些合适的漂亮东西。

![](img/c38d55f649fc8eb5006efb3ef6930d65.png)

An 8×8 segment of the total panel. The display draws 40W at 5V with all pixels on at the same time.

该项目包括一个由 INS-1(инC-1)管构成的 8×48 矩阵显示器。这些微小的霓虹灯管直径为 6.5 毫米，通电后会发出明亮的橙色光点。只需要 100 伏和 0.5 毫安的照明，它们比著名的谢妮更容易驾驶。

[Pierre]决定全力以赴，希望复制 WS2812 等智能 led 的功能。每个 LED 都内置了一个微控制器，所以[Pierre]也必须这样做。384 个霓虹灯管中的每一个都有自己定制的 PCB，包含 PIC16F15313 微控制器、升压电路和 6 引脚连接器。(哇哦！)当每个灯泡被焊接到它的 PCB 上时，它们就被插到底板。然后使用 ESP32 来驱动整个显示器。

以这种方式制作显示器需要大量的工作，其中大部分是焊接 384 个单独的灯泡印刷电路板，每个电路板包含 11 个组件。我们非常尊重[皮埃尔]的职业道德，在封锁期间完成了这项工作，最终的结果是一个辉煌的复古霓虹灯矩阵显示。我们最近还推出了其他霓虹灯矩阵。休息后的视频。

 [https://www.youtube.com/embed/fUn0hQzyqzI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/fUn0hQzyqzI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

