# Arduino 上的经典 DOS 游戏？

> 原文：<https://hackaday.com/2022/10/17/classic-dos-games-on-an-arduino/>

我们已经有一段时间没有看到 86Duino 了，但[TheRasteri]提醒了我们，他的视频[展示了如何使用它来运行经典的 MS-DOS 游戏](https://www.youtube.com/watch?v=ER3wFQB3pD0)。公平地说，这台电脑并不是真正的 Arduino，它本质上是一台安装在 Arduino 风格 PCB 上的微型 486 PC。

如果只是在一台微型电脑上运行 DOS 游戏，那就没什么新闻价值了。然而，主板本身没有显卡，而且正如[ther astri]指出的，声卡兼容性也是一个问题。然而，载板上有一个小小的 VGA 卡，由于另一个用户的一些工作，如果你想插入传统的声卡，可以在板上添加 ISA 总线。

ISA 黑客攻击做得很干净利落，但是有点复杂。如果您有适合该总线的卡，可以使用 PC/104 背板，而不是使用普通的 ISA 背板，从电气上来说，它们是一样的。该板能够以每秒近 30 帧的速度运行《毁灭战士》和《T2 之战》。还不错。不过，他在让鼠标工作时确实遇到了问题。

看着他用 QBasic 直接写入 ISA 卡上的寄存器，我有点怀念过去了。如果你想要一台旧的 DOS 机，又不想占用太多空间，这可能是你的不二之选。尤其是当你需要它来运行一些与现代计算机不兼容的旧硬件时。我们不得不怀疑是否有人会用这样的东西制作 USB 转 ISA 适配器。车手似乎是最难的部分。

大约 10 年前，我们看到了 86 duino,当时还有一些其他的 x86 单板计算机。显然，很多人[想经营复古游戏](https://hackaday.com/2015/07/03/tiny-x86-systems-with-graphics-cards/)。

 [https://www.youtube.com/embed/ER3wFQB3pD0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ER3wFQB3pD0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

