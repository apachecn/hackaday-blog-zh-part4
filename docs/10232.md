# 自驾还是精神控制？你喜欢哪一个？

> 原文：<https://hackaday.com/2021/05/24/self-driving-or-mind-control-which-do-you-prefer/>

我们知道你和我们一样喜欢好的生物黑客，所以我们认为你会喜欢脑波控制的遥控卡车。他认为他可以使用 [NeuroSky 的意识波](https://hackaday.com/2020/12/09/mind-controlled-beer-pong-gets-easier-as-you-drink/)，而不是自己制作脑电图。脑电图是非常复杂的多频波，需要一些相当复杂的电路和更复杂的信号处理来解释。所以，[托尼]认为卸下一点重担会很好，对他来说幸运的是，[mind wave 耳机对黑客相当友好](https://hackaday.com/2011/04/22/mindwave-is-developer-read-hacker-friendly-mind-control/)。

脑电图是一个非常活跃的研究领域，因此信号的一些更精细的细节仍在争论中。然而，似乎可以通过测量阿尔法波来量化[注意力，阿尔法波是 8-10 赫兹](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0214507)之间的脑电图内容。[而且似乎眨眼也可以从脑电图中提取出来](https://hackaday.com/2013/06/20/building-a-blink-based-input-device/)。方便的是，MindWave 将这些能量水平输出到一个附带的智能手机应用程序，然后[Tony]使用非常流行的 HC-05 模块通过蓝牙连接到他的 Arduino。

为了控制汽车，他利用现有的遥控器，而不是自己制作。像大多数人一样，[Tony]想过将 Arduino 引脚连接到遥控器上的按钮，从而绕过物理按钮，但他注意到按钮比他舒适焊接的按钮小一些，他不想冒险损坏电路板。[托尼的]遥控卡车有一个手枪式握把发射器，这启发了一个略有不同的方法。他将伺服系统安装到控制器的车轮机构上，允许他通过使用伺服系统旋转车轮来控制卡车的方向。然后，他在发射器上制作了另一个伺服系统，这样伺服系统可以在旋转时踩下油门。我们认为这是一个非常好的解决方法。

很酷的项目，[托尼]！在之前，我们已经看到了一些很酷的 EEG Hackaday 奖项。也许这是下一个大事件。

 [https://www.youtube.com/embed/E9g2Yh3_GVI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/E9g2Yh3_GVI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

