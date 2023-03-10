# 复音模拟/数字合成器项目

> 原文：<https://hackaday.com/2018/10/21/the-polyphonic-analog-digital-synth-project/>

[Matt Bradshaw]的 Hackaday 奖参赛作品是 [Polymod](https://hackaday.io/project/160626-polymod-modular-digital-synthesizer) ，这是一款模块化数字合成器，结合了模拟合成器的模块化和数字合成器的强大功能。每个模块(LFO、包络发生器、放大器等。)通过音频电缆连接到其他人，然后对结果进行数字处理以创作音乐。

合成器由一个玩具键盘组成，每个按键下面都有一个触摸开关，装在一个木箱里，这个木箱是从街上的书架上翻过来的。每个模块都是一系列带有木质面板的电位计和 I/O 插孔。模块连接到主板上的插座，并用指旋螺钉固定到位，这样就可以很容易地将模块切换出去。每个模块可以使用音频电缆连接到其他模块，就像模块化模拟合成器的连接方式一样。

主板包含一个 Teensy 3.6 和一个 Teensy 音频适配器为合成器创建音频。[Matt]编写的软件在 Teensy 上运行，允许数字合成器以单音或复音模式运行。在和弦模式下，软件会创建每个模块的数字副本，以便弹奏和弦。Teensy 扫描多达八个模块插座，对于它找到的每个模块，它读取电位计值以及 I/O 插孔的状态。键盘按钮被转换成控制电压，该控制电压可以被发送到任何模块以产生旋律。

[Matt]创造了一个伟大的合成器，它结合了模拟和数字合成器的优点，结果是一个廉价的模块化合成器，可以创造一些非常酷的声音。休息之后看看视频。与此同时，看看这个[乱七八糟的电线](https://hackaday.com/2017/02/24/a-mess-of-wires-turned-into-an-analog-synth/)和这篇关于一系列[开源合成器](https://hackaday.com/2016/02/23/a-slew-of-open-source-synthesizers/)的文章。

 [https://www.youtube.com/embed/LU9rVg5asSk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/LU9rVg5asSk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/vkGMGA4hJrk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/vkGMGA4hJrk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)