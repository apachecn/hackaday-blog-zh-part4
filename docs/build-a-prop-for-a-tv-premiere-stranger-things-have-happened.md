# 为电视首映式制作道具？更奇怪的事情发生了

> 原文：<https://hackaday.com/2022/05/25/build-a-prop-for-a-tv-premiere-stranger-things-have-happened/>

有些人运气很好。[Guy Dupont]有幸为某个电视节目的红毯首映式制作了一部实用的交互式壁挂式座机。这款手机将会是 80 年代风格披萨店的复活节彩蛋。大约每两分钟，电话就会响起，任何有勇气接听的人都会收到一份假的披萨订单、一条旧的答录机留言，或是一段不能提及的节目片段。

[![](img/493ee17bde1ebe02160e2ef02ded8748.png)](https://hackaday.com/wp-content/uploads/2022/05/ST-phone-inner.jpg)

Lots of room inside those old housings.

所以电话不能用了——能用了，但是怀旧情绪很强烈——在电话不响的时候拿起听筒会听到拨号音，按下按钮会听到忙音。那些旧的令人愉快但严厉的操作员录音会很酷，但只有这么多时间。您拨打的电话无法接通。请检查号码，然后重试。)

[Guy]使用 SparkFun RP2040 来处理来自 DTMF 键盘的输入，并向接收器的耳朵播放音调、拨号和忙音信号以及各种录音。

[Guy]没有使用驱动原来的铃声和钟声所需的高电压，而是使用一个小扬声器来播放铃声。所有东西都靠塞在键盘下的 8 个 aa 运行，键盘上的电压降到 5 V。

这个项目是在相当戏剧性的压力下完成的，这使得在休息后观看构建视频更加令人兴奋。只有五天的时间让电话工作起来，并在邮件中，[盖伊]躲藏在他办公室的地板上，这是他从一个被 COVID 困扰的房子中凌乱的移动避难所。不幸的是，整个比萨店的事情失败了，所以[盖伊]的手机不会出现在红地毯上。但至少它在网站上是黑白的，到处都是。

[Guy]对旧技术/新规格游戏并不陌生。还记得那次他把 Spotify 硬塞进 iPod Classic 吗？

 [https://www.youtube.com/embed/cjzxD0_v9hM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/cjzxD0_v9hM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

