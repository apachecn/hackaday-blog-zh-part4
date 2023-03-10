# 树莓圆周率龙头把圆周率的数字放在龙头上

> 原文：<https://hackaday.com/2021/04/06/raspberry-pi-spigot-puts-digits-of-pi-on-tap/>

圆周率日你做了什么？玩你的树莓 Pi 400？吃一些比萨饼或其他典型的圆形物体，背诵你已经记住的所有九个数字？这就是我们今年的情况。但不是[bornach]，不，[bornach]全力以赴，建立了一个龙头，它喷出的圆周率数字远远超过前九位小数。

这个聪明的龙头雕塑实现了[龙头算法](https://en.wikipedia.org/wiki/Spigot_algorithm),用于在一个 8×8 矩阵链的流中一个接一个地生成 Pi 的数字，并且使用了一个 Raspberry Pi(当然)。spigot 算法的要点是通过重用变量在任何给定时间存储尽可能少的数字。我们喜欢数字在矩阵上具体化的方式，就好像它们是被水激活的墨水。休息之后，请务必查看构建和演示视频。

顶部的 10k 电位计确实控制水龙头，因为 Pi 没有 ADC，所以[bornach]使用电位计给电容器充电，并使用达到阈值所需的时间来决定水龙头是打开还是关闭。这里有一些黑客攻击，包括冰棒棒 LED 矩阵支撑和帽子[bornach]造型，以便菊花链 8×8 LED 模块可以与 Pi 接口。

我们喜欢这里各个时代的树莓派，尤其是可爱的新皮可。虽然很小，但如果你不介意失去几个 GPIO 引脚，Pico 可以用钢锯切成更小。

 [https://www.youtube.com/embed/zqEtR9f9NLo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/zqEtR9f9NLo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

