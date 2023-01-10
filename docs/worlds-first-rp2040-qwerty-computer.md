# 世界首款 RP2040 QWERTY 电脑

> 原文：<https://hackaday.com/2021/05/28/worlds-first-rp2040-qwerty-computer/>

独立硬件开发人员[bobricius]又来了，制造了他声称的世界上第一个 Pico RP2040 QWERTY + IPS 开发套件——Pico computer。这是一种手掌大小的计算机。它集成了一个由触觉按钮开关制成的键盘、一个 TFT IPS 显示器和一个 RP2040 微型计算机模块。它的尺寸为 100 x 65 毫米，比典型的 ISO-7810-ID-1 大小的信用卡略大，比 A7 纸略小。

[Bobricius]该项目的目标之一是最大限度地减少外部组件的数量，从而最大限度地利用 RP2040 的内部功能。如果你仔细阅读张贴在他的 GitHub 库上的示意图，你会同意他肯定已经达到了这个目标。可选的 LoRa 模块有一个滤波电容，两个 MOSFETs 和三个电阻驱动扬声器和 TFT 背光。除了连接器、开关和子模块本身，就是所有的外部电路。

两个 USB 连接器(C 型用于电源，微型 USB 用于数据)的排列是连接器/模块放置的一个有趣方面。他计划在未来增加一个以太网模块，并发布更多的修订以修复小错误，并使前面板适合更多尺寸的显示器。我们想知道电池模块附件是否也在工作中。

如果你认识[bobricius]，那是因为他之前的[ARMA chat 手持 LoRa messenger 项目](https://hackaday.com/2020/04/25/a-lora-im-me-for-the-end-of-the-world/)是去年 Hackaday 社区投票(Bootstrap)获奖者之一。我们认为微型键盘对他来说可能是一种困扰——事实上，他坦率地承认被自己的热情蒙蔽了双眼。例如，看看他 2018 年的[迷你(Pi)QWERTY USB 键盘](https://hackaday.io/project/158454-mini-piqwerty-usb-keyboard)。感谢[Itay]通过[黑客热线](https://hackaday.com/submit-a-tip/)让我们关注这个项目。

 [https://www.youtube.com/embed/pJGlxj9I5Sg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/pJGlxj9I5Sg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2021](https://prize.supplyframe.com) is Sponsored by:[![Digi-Key](img/e7d13a315fd6226594212ca8f8762832.png)](https://www.digikey.com/)[![Supplyframe](img/fdb8a432506edeeafacfef227b3d3b33.png)](https://supplyframe.com/)