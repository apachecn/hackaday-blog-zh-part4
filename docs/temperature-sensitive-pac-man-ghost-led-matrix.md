# 对温度敏感的 Pac-Man/Ghost LED 矩阵

> 原文：<https://hackaday.com/2022/07/09/temperature-sensitive-pac-man-ghost-led-matrix/>

如果你像我们一样，你永远不会厌倦复古游戏灵感的项目，动态二人组，[monsely]，似乎也喜欢他们。他们的[温度敏感的 Pac-Man/Ghost LED 矩阵](https://www.instructables.com/PacmanGhost-LED-Matrix/)将成为任何游戏爱好者的绝佳桌面显示器。

首先，他们在好的纸笔上画了一些草图，整理出他们需要的所有发光二极管，并找出连接。这么多 led，协调是非常重要的[否则你很快就会弄得一团糟](https://hackaday.com/2019/07/31/big-ol-led-wall-looks-cool-can-draw-over-170-amps/)。幸运的是，WS2812/Neopixel 风格的 LED 灯条最大限度地减少了大多数必要的连接，因此这是一种解脱。这些 LED 灯条只需要一个 GPIO 来控制，这使得用一个非常基本的微控制器就能轻松完成这个项目。

仅仅显示一个动画图形对[monsely]来说有点太简单了。他们决定让鬼魂对温度敏感，如果外面冷就变成蓝色，如果暖和就变成红色。当然，你可能想根据你住在哪里或者你的 [HVAC 系统如何运行](https://hackaday.com/2016/03/28/hvac-techs-hackers-who-make-house-calls/)来调整阈值。吃豆人保持经典的黄色，这是我们所期望的。

当然，没有合适的外壳，任何好的桌面显示器都是不完整的。[monsely]选择了一个纸板盒，但我们相信你可以激光切割或打印一些更坚固、更美观的东西。但是，嘿，不管怎样，对吗？