# 值得企业使用的 Arduino 医务室显示器

> 原文：<https://hackaday.com/2019/07/05/an-arduino-sickbay-display-worthy-of-the-enterprise/>

《星际迷航》中的各种显示器和界面，尤其是《T2》原版系列中的各种显示器和界面，被有意设计成迟钝和过于复杂的，这样它们对观众来说就显得很超前。如果你能弄清楚苏鲁是如何用一系列无标签的按钮和摇杆开关驾驶*企业号*飞行的，我们很想听听。但船上的一个地方让这种抽象的设计美学有点退缩，那就是医务室，因为他们可能希望观众一眼就能明白柯克或斯波克是否会度过他们最新的死亡之旅(剧透:他们很好)。

[![](img/021a7f27f937a122ca401b2f45e2a4d1.png)](https://hackaday.com/wp-content/uploads/2019/07/sickbay_detail.png) 在他的最新项目中，[【XTronical】用一台 Arduino Nano](https://www.youtube.com/watch?v=0zNeVVHoLgE) 和一个 2.8 英寸的液晶显示器重现了麦考伊医生医务室的经典显示器。它甚至有一个扬声器和 MP3 播放器模块来重现原始节目的“心跳”声音。整个东西看起来和听起来都很棒，对于经典的《星际迷航》迷来说是一个完美的桌面玩具。但这不仅仅是一个玩具，这是一个全功能的医疗扫描仪。

当然，这个小工具不能告诉你是否患有严重的里格氏热，但它可以使用 MAX30100 脉搏血氧计模块和 DS18B20 温度计读取你的生命体征。事实上，它实际上有两个 DS18B20 传感器:一个测量环境温度，另一个测量皮肤温度。有了这两个数字，[XTronical]说它可以计算出你的核心体温。唯一虚构的是闪烁的“呼吸”指示器，那只是一个估计。

那么，我们该何去何从呢？这个项目仅仅是建造一个完整道具的第一步，也许是以医用三录仪的形式。[这些年来，我们已经看到了一些惊人的 TOS tricorder 构建](https://hackaday.com/2018/03/19/building-a-tricorder-prop-worthy-of-mr-spock/)，一些[甚至使用树莓 Pi 将一些功能硬塞进其中](https://hackaday.com/2017/08/18/picorder-raspberry-pi-stands-in-for-stone-knives-and-bearskins/)。[XTronical]说他正在将源代码和一步一步的构建指南放在一起，所以请在不久的将来密切关注。

 [https://www.youtube.com/embed/0zNeVVHoLgE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/0zNeVVHoLgE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

