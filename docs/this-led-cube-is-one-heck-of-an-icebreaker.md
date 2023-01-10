# 这个 LED 立方体是一个破冰船

> 原文：<https://hackaday.com/2019/09/05/this-led-cube-is-one-heck-of-an-icebreaker/>

就像制造商的口味一样，LED 立方体有各种形状和大小。从最简单的 3x3x3 微控制器测试，到更高级的定制安装，它们是学习一系列有用的嵌入式技术并同时炫耀的好方法。[kbob]已经完全做到了这一点，[用他自己的闪闪发光的立方体构建了](https://kbob.github.io/2019/08/23/led-cubes)，并在[发布了一个包含所有文件的存储库](https://github.com/kbob/LED-Cube)。

就像一群来自魔多的兽人一样，[kbob]的魔方就是关于数量的力量。每边长 136 毫米，由 64 x 64 P2 面板构成，每边封装 4096 个 led，共 24，576 个。Raspberry Pi 用于运行节目，允许运行各种动画。不幸的是，它缺乏足够的马力以合适的帧速率运行这么多 led。相反，它与破冰船 FPGA 合作，可以毫不费力地为面板生成所需的 HUB75 信号。

由于微型发光二极管的高密度和动画的平滑帧率，最终的效果相当华丽。[kbob]指出，实际上有很多人在从事类似的破冰者项目；[最近[Piotr]的一段视频给人印象特别深刻。](https://twitter.com/esden/status/1160309492896215040)

LED 立方体很可能在一段时间内仍然是一种主要形式，我们迫不及待地想看看社区接下来会出现什么。如果你想变得更有趣，你甚至可以加入一些 OpenGL。休息后的视频。

> 破冰船 LEDCube。这是一个吸引注意力的地方。我很高兴你们这么多人喜欢它。感谢[@ kernlbob](https://twitter.com/kernlbob?ref_src=twsrc%5Etfw)[@ TNT](https://twitter.com/tnt?ref_src=twsrc%5Etfw)[@ GeorgeIoak](https://twitter.com/GeorgeIoak?ref_src=twsrc%5Etfw)[@ vifino](https://twitter.com/vifino?ref_src=twsrc%5Etfw)[@ zzaurak](https://twitter.com/zzaurak?ref_src=twsrc%5Etfw)等许多人的启发和努力让它成为现实。:)[pic.twitter.com/2ZIiwj5L1v](https://t.co/2ZIiwj5L1v)
> 
> —Piotr es den-Tempski es den @ chaos . social(@ es den)[2019 年 8 月 10 日](https://twitter.com/esden/status/1160309492896215040?ref_src=twsrc%5Etfw)