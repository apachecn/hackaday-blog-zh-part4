# 附加物变成电致发光的

> 原文：<https://hackaday.com/2019/04/17/add-ons-go-electroluminescent/>

又到了一年中的这个时候，我们再次面对 Badgelife 的最新创新，探索电子和制造的艺术价值的运动。这是一块电致发光印刷电路板，是我们见过的最好的作品。[它也是一个低劣的附件](https://hackaday.com/2019/03/20/introducing-the-shitty-add-on-v1-69bis-standard/)会发蓝光。

令人惊讶的是，在印刷电路板上应用电致发光涂层的过程，我们之前已经讨论过了。去年年底，[【本·克拉斯诺】深入研究了一种 DIY EL 显示器](https://hackaday.com/2018/11/26/applied-science-rolls-an-electroluminescent-controller/)。这个过程很昂贵，但是所有的产品都来自一家名为 [Lumilor](https://www.lumilor.com/) 的公司。这个过程的第一步是用喷枪在基底上涂一层薄的导电涂层。由于印刷电路板的整个想法是将一层导电材料蚀刻成你想要的任何形状，所以简单的电路板是玩 EL 显示器的理想实验平台。传统上，EL 显示屏完全是用丝网印刷工艺制作的，就像[Fran]正在试图[重现阿波罗 DSKY 显示屏](https://hackaday.com/2017/05/29/re-creating-the-apollo-dskys-display/)。

这个徽章的电子设备只是一个微型芯片 MIC4832 EL 驱动器，它将来自附加插头的 3 . 0 伏左右的电压转换成数百赫兹的 100 伏左右的交流电。这是一种驱动 EL 显示器的单芯片解决方案，您只需要一个电感、二极管和一些电容和电阻。ATtiny85 可以用来闪烁电路，或者，你可以复制[Ben]的工作，建立一个字符 EL 显示器。

将电致发光涂层应用到 PCB 上的过程确实需要喷枪或喷枪，并且化学品有点贵。然而，这拓展了艺术印刷电路板的应用范围。这是技术的新应用，简单来说就是可穿戴电子产品。这是媒介的可能性的最好例子，也是来自 Badgelife 场景的一些最好的作品。