# PoE 为圣诞灯供电，但却开启了更多

> 原文：<https://hackaday.com/2019/12/31/poe-powers-christmas-lights-but-opens-up-so-much-more/>

可寻址的发光二极管是我们社区自制圣诞装饰品的主要部分，这些发光二极管的微处理器控制也是如此。所以第一眼看上去，LED 装饰圣诞树看起来很漂亮，但并不特别特别。但是在阅读了他的文章后，你会发现这个项目远比看上去的要多，并了解到许多关于它背后的技术，这些技术远远超出了节日灯光表演的范围。

该装饰完全由以太网供电，PIC 微控制器将以太网 DMX 数据包转化为 LED 灯串的命令。控制板是从头开始设计的，包括所有的 PoE 电路，这篇文章非常全面地介绍了这种电源，使读者不再将 PoE 仅仅视为另一个现成的黑匣子。一路上，我们看到了他的所有代码，以及学习一些有趣的花絮，如使用包含唯一 MAC 地址的预编程 EEPROM。

因此，如果你的房子有 CAT5 电线，你想为你的节日光彩增加一个额外的维度，你有整整一年的时间来建造自己的版本。他以前在这里出现过，用他的蜂鸣器打破了大写锁定的习惯。

 [https://www.youtube.com/embed/0Oo144LTxu4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/0Oo144LTxu4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

