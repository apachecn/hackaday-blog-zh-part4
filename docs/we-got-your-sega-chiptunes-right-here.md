# 我们这里有你的世嘉芯片音乐

> 原文：<https://hackaday.com/2018/10/04/we-got-your-sega-chiptunes-right-here/>

Chiptunes 很酷，但当你进入其中时，你会意识到你主要是在处理准将 SID tunes，Atari POKEY 为酷孩子准备的曲目，Game Boy 的哔哔声和 bloops，也许还有一些 nes 的曲目。还有另一个选择——世嘉 Genesis 中的声音芯片。这个东西可以打鼓，人类和 T2 为藏在经典 16 位游戏机中的和谐硅制造了完美的播放器。

[Aidan]之前已经基于 YM3812 芯片(SoundBlaster 和 Adlib 声卡中的雅马哈芯片)制作了一个微型音乐播放器。世嘉创世纪[雅马哈 YM2612](https://en.wikipedia.org/wiki/Yamaha_YM2612) 内部的芯片有点不同。这种芯片的杀手锏是 PCM 波形，它不是以简单的小代码存储的。这些是发送到芯片 DAC 的大量二进制数据。例如，*的《刺猬索尼克》*的 SEGGGGAAAA intro 使用了八分之一的弹夹空间。你不会用一个小小的微控制器和 20kB 的内存来建造一个世嘉芯片播放器。

该解决方案采用外部 SPI RAM 器件的形式。23LC1024 的大小是整整 1 兆位，由于它是 SPI，它的速度足以跟上采样速度。其余的电路包括混频器，前置放大器和功率放大器是基于创世纪的实际原理图，SD 卡和有机发光二极管扔在良好的措施。听起来怎么样？在广告下面有一个很棒的视频，是的，索尼克 3 的配乐听起来和二十年前一样好。

 [https://www.youtube.com/embed/WoAp2-gWaLM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/WoAp2-gWaLM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

