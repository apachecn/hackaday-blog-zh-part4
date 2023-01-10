# 把一切都变成水龙头控制器

> 原文：<https://hackaday.com/2018/08/21/turning-everything-into-a-tap-controller/>

我们的一生都在盯着发光的矩形，而我们的周围都是坚硬平坦的表面。[Ben]有想法将这些平坦的表面变成一个通用的 tap 接口控制器，他的 Hackaday 奖项目可能会做到这一点。

进入这个项目的一些现有技术包括 [Ping Pong Plus Plus](https://github.com/xiaosquared/PingPongPlusPlus) ，这是一种乒乓球的增强现实实现，可以在乒乓球击中桌子的任何地方投射光线。这款游戏通过在桌子底部安装压电元件来实现这一点，只需要一点数学运算就可以确定球击中了桌子的哪个位置。[还有 MicLoc](http://ruralhacker.blogspot.com/p/micloc.html) ，一种对敲门有反应的门锁。

对于这种现有技术，一切都与微控制器和外设有关，为此，[Ben]转向了 STM32F303RE，它内置四个非常快速的 ADC 和运算放大器。上面有很多 DMA 的使用，代码使用了大量的信号处理。这里重要的一点是找到桌面上相当于地震的 P 波和 S 波之间的差异——本只想要纵向穿过桌子的波形的第一部分，而不是整个桌子更大的振动。

如果[本]设法把这些组合在一起，整面墙就可以成为一个电灯开关或调光器。你可以在你的门上加一个暗号，你的桌子可以控制你的电脑。这是一个很有前途的想法，这个项目的工程设计非常棒。

The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)