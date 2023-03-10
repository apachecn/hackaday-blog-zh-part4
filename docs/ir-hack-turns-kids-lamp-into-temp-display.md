# 红外黑客把孩子的灯变成温度显示器

> 原文：<https://hackaday.com/2019/11/02/ir-hack-turns-kids-lamp-into-temp-display/>

有时候，对现成产品的巧妙破解可能来自于对它的拆卸和硬件修改，但在其他时候，最优雅的破解甚至可以不用螺丝刀就能完成。[Brian Lough]被一个朋友要求复制一个随温度变色的商用儿童夜灯，他的回应是使用一个现成的变色儿童灯，不加修改，[通过它的红外控制](https://www.youtube.com/watch?v=XoMP9PrHlis)向它发送与温度相关的颜色命令。

他的设备在硬件方面非常简单，使用现成的 Wemos D2 Mini ESP8266 板，运行 Arduino bootloader，再加上 BME280 温度传感器、IR 接收器和发射器。我们把他的视频放在了 break 下面，这对任何对红外逆向工程感兴趣的人来说都是一个方便的入门，我们可以看到，它可能会引发其他项目。对于那些足够好奇的人来说，[它可以在 GitHub](https://github.com/witnessmenow/Temperature-Night-Light) 上找到。

[Brian]在这里出现了很多次，绝对值得一去。他最近的一个作品突出了另一个孩子的玩具[,使它变得非常特别。](https://hackaday.com/2019/04/14/bringing-a-childs-play-kitchen-to-life/)

 [https://www.youtube.com/embed/XoMP9PrHlis?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/XoMP9PrHlis?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

