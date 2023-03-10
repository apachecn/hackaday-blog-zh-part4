# 来自 Teensy 的优雅鼓机

> 原文：<https://hackaday.com/2018/10/20/elegant-drum-machine-from-teensy/>

打鼓很难，尤其是对不协调的人来说。同时做四件事，同时保持均匀的节奏，对我们大多数人来说是不合理的。然而，与其为你的乐队雇佣一个精通这种艺术的鼓手，你可能会选择将这项工作外包给一台机器。它更便宜，也不太可能导致[自燃](https://www.youtube.com/watch?v=tZrqC5LL_oo)。

这个鼓机其实就是一个 MIDI 欧几里德音序器。欧几里德节奏就其本身而言是有趣的，但基本原理是找到两个节拍之间的共同点，以便自动生成复杂的节拍。这个特殊的单元运行在 Teensy 3.5 上，由四个 RGB 旋转编码器、一个 SSD1306 LCD、四个瞬时按钮和四个 16 LED Neopixel 环组成。设置每个转盘可以增加特定通道的节拍数，并且可以配置几乎无限的节拍和模式组合。

要真正感受这里发生了什么，休息后看看视频是值得的。MIDI 也是一个迷人的标准，除了它是 80 年代创建的少数几个仍在积极使用的标准之一这一事实之外，它还可以用于构建各种有趣的乐器，如[用木槌敲击酒杯](https://hackaday.com/2018/07/31/the-precise-science-of-whacking-a-wine-glass/)或[定制合成器](https://hackaday.com/2018/06/09/monotron-gets-all-the-mods/)。

感谢[baldpower]的提示！

 [https://www.youtube.com/embed/aqOsPZUo860?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/aqOsPZUo860?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

