# Chris Gammell 谈论电路工具箱

> 原文：<https://hackaday.com/2019/02/11/chris-gammell-talks-circuit-toolboxes/>

Chris Gammell 想知道:你的电路工具箱里有什么？

就我个人而言，我的库存有点不足。我确实知道，在我的一篇日记中，可能是在 20 世纪 80 年代，我草草写下了我刚刚构建的电压倍增器的原理图，采用经典的二极管和电容梯形拓扑结构。我可能用一个小的钟形变压器给它供电，我可能得到了一百伏左右的电压。当时我非常自豪，我把它写下来给后人，并附上一张纸条:“这是我今天做的！”

我认为[克里斯 2018 年 Hackaday 超级大会演讲](https://www.youtube.com/watch?v=TsrRr4Iq6_M)的整个要点正是我在做出我的“发现”时试图得到的东西——我们都有只为我们工作的电路，你拥有的越多越好。大多数读者会从一些地方认出克里斯，如[的 Amp Hour](https://theamphour.com/) ，他和达夫·琼斯主持的每周播客，以及[他的 KiCad 教程视频](https://www.youtube.com/user/contextualelectronic/playlists)。Chris 从事电气工程已经将近 20 年了，他收集了一些常用电路，这些电路不断出现在他的设计中，让生活变得更加轻松，他很有礼貌地与大家分享了这些电路。

[![](img/4072611c1b5cf71bfd8cd6529b7bd766.png)](https://hackaday.com/wp-content/uploads/2019/01/907a2107.jpg) 正如克里斯指出的，正是这些小小的电路造成了不同。[他演讲的一张又一张幻灯片](https://chrisgammell.com/improve-your-circuit-toolbox-simple-designs-that-will-save-your-next-product/)都是原理图，里面只有少数几个元件，涵盖了从非常简单的 LED 电源指示器和开关去抖到使用 74HC595 的 IO 扩展的应用。正如任何明智的工程师可能会做的那样，Chris 的工具箱包括一系列电源保护电路，从使用 MOSFET 和齐纳二极管的极性反转保护，到使用差分放大器和光隔离器的小巧高端驱动器关断，应有尽有。

我最喜欢的部分是“无代码”部分——你可以用分立元件做些什么，让微控制器电路变得更好。我们看到“你可以用 555！”读者的评论，克里斯同意，至少在某种程度上。他恰当地指出，微控制器可以在 IO 引脚处于未知状态时被唤醒，并提供了几种电路来防止潜在的危害，例如施密特触发器上电复位或简单地添加一个下拉电阻来默认 MOSFET 处于安全状态。代码可以完成很多工作，但只需增加几个部分就可以让电路变得更加安全和有用。

Chris 承认，在任何受众中，每个人在硬件学习曲线方面总是处于不同的位置，因此对一些人来说是旧的东西对另一些人来说可能是新的启示。尽管如此，在某些时候，对某些人来说，一切都是新的，这通常是把它写下来的最佳时机。这就是我多年前用电压倍增器做的事情，结果它从未离开过我。这是一个很好的建议，如果您还没有开始构建自己的电路工具箱，现在正是时候。

 [https://www.youtube.com/embed/TsrRr4Iq6_M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/TsrRr4Iq6_M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

