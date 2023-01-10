# 钢琴家章鱼

> 原文：<https://hackaday.com/2019/06/12/the-pianist-octopus/>

MIDI 已经有近四十年的历史了，但是如果你有一个没有 MIDI 的旧‘玩具’键盘，你会怎么做？或者任何让它听起来不错的方法？你可以把它变成一架钢琴，而这正是亚历山德罗对一个旧玩具键盘所做的。这是钢琴家章鱼，它可能是你见过的最酷、最整洁的钢琴家。

这个建筑使用了 24 个独立的 9 克业余爱好伺服系统，这当然意味着你需要以某种方式驱动这些伺服系统。有很多方法可以在 Arduino 板上安装一些伺服系统，但是当你需要驱动 24 个伺服系统时，你的选择就变得有些有限了。电子设备主要由[鱼章鱼](https://www.fishino.it/octopus.html)组成，一个 Arduino 防护罩可以驱动 16 个单独的伺服系统。在 Arduino 上安装两个这样的护盾，你就有了可以驱动 24 个伺服系统的东西。

该建筑的机械部分由一个 3D 打印框架组成，允许伺服系统跨弧安装，有点像竖琴。金属杆将伺服系统连接到触手状的致动器上。这些是在 Google SketchUp 中设计的，用 PLA 打印的。

连接到这些伺服系统和 Arduino 的是一个字符 LCD 和几个按钮，允许用户通过几个功能进行循环。播放按钮播放当前的旋律(顺便说一下，是基于老诺基亚的铃声)，还有几个按钮调整个人伺服的位置，还有一个按钮停止播放。由于这是一个玩具钢琴的完整的电子-机械接口，MIDI-in 端口不是不可能的；MIDI 实现需要做的就是在音符开事件时向下移动伺服，在音符关事件时向上移动伺服。

The [HackadayPrize2019](https://prize.supplyframe.com) is Sponsored by: [![Supplyframe](img/79a7db035b8a2b6c2b7b0895c45b7de8.png)](https://supplyframe.com/)  [![Digi-Key](img/ba094a14c430ab81591a2abdc54a5363.png)](https://hackaday.io/digikey)  [![Microchip](img/5023ef0b7ff1aee311cba9b54a3ac9fe.png)](https://hackaday.io/microchip)