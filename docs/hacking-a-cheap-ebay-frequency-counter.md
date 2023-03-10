# 黑进一个便宜的易趣频率计数器

> 原文：<https://hackaday.com/2019/04/30/hacking-a-cheap-ebay-frequency-counter/>

易贝是一片神奇的土地，到处都是状况不佳的星球大战纪念品，疯狂加价的旧游戏机，以及数量惊人的 DIY 电子产品。[TheHWCave]发现自己在摆弄一个普通的频率计数器套件，[并决定在这个过程中做一些选择改进(Youtube 链接，嵌入在下面)。](https://www.youtube.com/watch?v=0D6EcgTQtNw&feature=youtu.be)

问题中的频率计数器是[【Wolfgang“Wolf”büscher】的极简 PIC 设计](https://www.qsl.net/dl4yhf/freq_counter/freq_counter.html)的普通克隆版本。使用 PIC16F628 和一些七段显示器，它是一个通用的频率计数器。克隆版本通常增加一个晶体振荡器测试仪，在易贝可以以相当低的价格买到。

[TheHWCave]发现这些修改没有多大用处，于是开发了一种方法，将测试器组件转变为更有用的信号前置放大器。不满足于此，定制固件被开发出来，既提高了分辨率，也增加了转速表功能。这使得该装置能够以每分钟转数显示其输出，而不是简单地以赫兹显示。通过与光学传感器或其他转速信号相结合，它可以方便地显示转速。如果你对这个理论不熟悉，[仔细阅读我们的光度计初级读本](https://hackaday.com/2017/03/17/how-to-use-a-photo-tachometer/)。如果你想修改你自己的套件，[Github 上有修改过的固件。](https://github.com/TheHWcave/PIC-freq.counter-modification/)

[在](https://hackaday.com/2019/01/10/transistor-tester-becomes-car-display/)之前，我们已经看过其他易贝套件的特别改装。便宜和使用商用微控制器使它们成为黑客攻击的成熟平台，无论你只是想做一些调整还是完全改变设备的用途。

【感谢 Acesoft 的提示！]

 [https://www.youtube.com/embed/0D6EcgTQtNw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/0D6EcgTQtNw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

