# 一个开源玩具合成器

> 原文：<https://hackaday.com/2018/10/12/an-open-source-toy-synth/>

如果你认为电子乐器的未来是巨大的艾默生级模块化合成器，带有跳舞机大小的垫子的巨型 MPC，或者昂贵的 polysynths，那你就大错特错了。实际上，未来是玩具。那些可以装进口袋的小 Korgs 卖得很火，口袋经营者是山中之王。更有趣的音乐玩具之一是[风琴](https://www.critterandguitari.com/organelle)，这是一个铝制外壳，带有枫木按钮，呈键盘状。这是一个合成器，是一个声音引擎，它确实会产生一些有趣的噪音。所有的软件都是开源的，但硬件不是。这就让其他人为我们制造硬件了。这正是[【米切尔】为他的黑客奖参赛作品](https://hackaday.io/project/160754-puredata-portable-synth)所做的。

这个构建的核心是一个 Nanopi Neo 内核，或者基本上是一个具有 256 MB 内存、运行频率为 1.2 GHz 的 Allwinner H3 分线板。它运行基本的细胞器脚本，并拥有成为 MIDI 设备的所有驱动程序。除此之外，还有一个 DAC、一个小 TFT 屏幕、一个用于读取按钮、编码器和 pots 的 STM32F103、一个声卡、一个 USB 集线器 IC 和一个从 Kindle 上拆下来的电池。

这个项目的想法是沿着青少年工程 OP-1 的路线，另一个非常花哨的“玩具”合成器，但也要建立其他任何人都可以建立的东西。[mitchell]就在那里，他制作的原型 PCB 实际上可以工作。还有很多工作要做，但这是一个非常有趣的项目，我们迫不及待地想看到它的黄金时段。

The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)