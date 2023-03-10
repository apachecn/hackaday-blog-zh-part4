# 用 MIDI 控制一个坏掉的超级任天堂

> 原文：<https://hackaday.com/2020/09/19/controlling-a-broken-super-nintendo-with-midi/>

一个无法显示精灵的超级任天堂不会成为一个非常好的游戏系统。事实证明，当有名无实的英雄不可见时,*超级马里奥世界*就没那么有趣了。所以毫不奇怪几年前[jwotto]最终把这个部分功能的 SNES 扔进了零件箱。

但是他最近提出了一个项目，这个项目实际上可能受益于它不寻常的图形问题；[将故障控制台变成电路弯曲视频合成器](https://lookmumnocomputer.discourse.group/t/hacked-super-nintendo-video-synth/1767)。该系统已经显示出损坏的视觉效果，所以[jwotto]认为他可以通过探查内部并识别短路时产生有趣视觉效果的引脚来帮助解决问题。

[![](img/94c44aa2623fa67e81e3e2a2a438a324.png)](https://hackaday.com/wp-content/uploads/2020/09/snesmidi_detail.jpg)

Installing the new electronics into the SNES.

一旦他绘制出引脚，他就将它们全部连接到一个晶体管开关板上，这是他在之前的项目中提出的。这将让 Arduino 根据命令短路引脚，同时仍然保持微控制器与 SNES 相对隔离。然后就是写一些代码，让晶体管根据 MIDI 输入启动。

最终的结果是一个伴随着音乐产生视觉故障的 SNES，当[jwotto]做现场表演时，他可以将它连接到投影仪上。一个特别好的特点是，每个游戏都以自己的方式响应，所以他可以更换墨盒来显示完全不同的视觉效果，而不必改变任何 MIDI 序列。

像这样的一个项目是对电路弯曲和 MIDI 黑客的一个很好的介绍，对于任何想要尝试数字技术的人来说，[应该与 MIDI Game Boy Advance](https://hackaday.com/2011/08/11/adding-a-midi-input-to-a-game-boy/) 很好地匹配。

 [https://www.youtube.com/embed/iDArikhlg2Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/iDArikhlg2Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



【感谢不规则棚的提示。]