# Raspberry Pi 疯狂吉他钻机把你变成一个硬 N 重一个人的乐队

> 原文：<https://hackaday.com/2020/10/07/raspberry-pi-crazy-guitar-rig-turns-you-into-a-hard-n-heavy-one-man-band/>

这是一个常见的问题:你在一个聚会上，有一把吉他，你想用你的 Wonderwall 演奏技巧给每个人留下深刻印象的计划被太大的整体噪音水平所挫败。好吧，[Muiota betarho]不会再有那个问题了，从现在起，他会带着他的*疯狂吉他装备 2.0* ，一把原声吉他变成了电动的——以及更多——在他的 YouTube 频道上展示三集视频系列[。对于不耐烦的人来说，这里有](https://www.youtube.com/c/MuiotaBetarho/)[视频 1](https://www.youtube.com/watch?v=lbpCXK37ZCc) 、[视频 2](https://www.youtube.com/watch?v=3-UrHXt4qOE) 和[视频 3](https://www.youtube.com/watch?v=nguSpfvGxQk) ，但休息后你也会发现它们被嵌入。

为了开始这个系列，【Muiota betarho】在一把廉价的木吉他主体上增加了一个电吉他拾音器、一组扬声器、一个放大器板和一个电池组。然后，他拆卸了一个 [Zoom MS-50G 多效踏板](https://zoomcorp.com/en/jp/multi-effects/multistomp-pedals/ms-50g/)，并用 3D 打印的外壳将其重新组装到吉他上。将吉他、效果踏板、放大器和扬声器组合成一个独立的乐器会让这个项目变得非常棒，但这仅仅是个开始。

[![Touch screen and controls closeup](img/11802c61bc66cf75c271fd0d8f20cad3.png)](https://hackaday.com/wp-content/uploads/2020/10/crazy-guitar-rig-closeup.jpg)

RPi touch screen running SunVox, plenty of buttons, and integrated multi-effect pedal on the left

所以，[是时候添加一个运行](https://www.youtube.com/watch?v=3-UrHXt4qOE) [SunVox](https://warmplace.ru/soft/sunvox/) 的树莓 Pi 了，并在飞行中扔进一个触摸屏来控制它。SunVox 本身是免费的，但不幸的是不是开源的，跨平台合成器和跟踪器，[Muiota betarho]用它来添加鼓轨道和一些额外的乐器和效果。在最后一部分，当他将 SunVox 连接到 Raspberry Pi 的 GPIO 引脚时，他更进一步[。这使他能够自动切换缩放踏板上的效果，但也为外部设备提供 I/O 连接，如脚踏开关，或伴随他演奏的整个灯光表演。](https://www.youtube.com/watch?v=nguSpfvGxQk)

当然，[给原声吉他](https://hackaday.com/2016/08/03/rocking-an-acoustic-guitar-by-making-it-electric/)增加一个磁性拾音器，或者给原声乐器[通电，比如架子鼓](https://hackaday.com/2020/07/08/your-own-electronic-drum-kit/)，并不新鲜。使用单板机[作为效果踏板](https://hackaday.com/2013/01/28/raspberry-pi-becomes-a-guitar-effects-processor/)或[作为你口袋里的放大器](https://hackaday.com/2018/03/05/portable-guitar-amp-is-that-a-linux-in-your-pocket/)也不是。另一方面，将这一切集成到一个单一的设备中理所当然地为这款吉他赢得了它的*疯狂吉他装备*的名字。

(感谢提示，[alex]！)

 [https://www.youtube.com/embed/lbpCXK37ZCc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/lbpCXK37ZCc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent) 
 [https://www.youtube.com/embed/3-UrHXt4qOE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/3-UrHXt4qOE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent) 
 [https://www.youtube.com/embed/nguSpfvGxQk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/nguSpfvGxQk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)