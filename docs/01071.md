# 重新设计带亮灯按钮的音乐键盘

> 原文：<https://hackaday.com/2018/11/04/redesigning-the-musical-keyboard-with-light-up-buttons/>

钢琴的键盘没有意义。如果你想弹奏 F 大调和弦，只需连续敲击 F、A 和 C——所有的白键。如果你想弹奏 B 大调和弦，你可以按 B、D#和 F#。一把白钥匙，然后是两把黑钥匙。钢琴键盘不是同构的，这意味着相同质量的和弦有不同的形状。为了获得 Hackaday 奖，[CSCircuits]和他们的团队正在研究一种能让和弦变得直观的键盘。它被称为 Kord Kontroller ，这是一个连接到 Ableton 上看起来也不错的设备。

Kord Kontroller 的布局将所有的音阶度数排列在键盘顶部的五度圆圈中。要演奏 90%的西方音乐，你可以按一个 I 和弦按钮，向左移动一个 IV 和弦按钮，向右移动两个 V 和弦按钮。和弦质量由键盘底部决定，降三度、四度、九度、十一度和十四度按钮可替换或增强您想要弹奏的和弦中的音符。由于这是一个有效的 MIDI 控制器，有按钮来改变八度音阶和模式。

就硬件而言，这种键盘是由 [Adafruit Trellis 模块](https://www.adafruit.com/product/1616)构成的，这些模块是一个 4×4 的硅胶按钮和 led 网格，可以连接在一起，放在一条 I2C 总线上。[外壳](https://hackaday.io/project/161105-kord-kontroller)将这些按钮包裹成一个 3D 打印的按钮孔网格，经过一点工作和热熔胶，一切看起来都像它应该的那样。

这是一个有趣的音乐装置，被提名为[乐器挑战赛](https://hackaday.io/list/161904-thp-2018-semifinalists-musical-instrument)的决赛选手。你可以在下面看看一个带有果酱的演示视频。

 [https://www.youtube.com/embed/3fUL_Did77w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/3fUL_Did77w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)