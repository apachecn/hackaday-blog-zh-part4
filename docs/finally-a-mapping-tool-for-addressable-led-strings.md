# 最后，用于可寻址 LED 串的映射工具

> 原文：<https://hackaday.com/2022/03/23/finally-a-mapping-tool-for-addressable-led-strings/>

可寻址的 LED 灯串让制作各种有趣的动画项目变得前所未有的容易。但是，如果不使用简单的网格布局，则在代码中映射字符串可能会有点困难。不要担心，因为[杰森·库恩]提供了一个可以帮你摆脱困境的工具！

【杰森】的网络应用，[可在此访问。](https://jasoncoon.github.io/led-mapper/)用于在处理 WS2812B 等可寻址 LED 串以及 FastLED 和 Pixelblaze 等库时绘制不规则布局。如果你正在制作某种 LED 地球仪，疯狂的 LED 树，或者其他非网格形状，这个工具可以帮助你。

第一步是在 Google Sheets 表格中创建 led 的布局，然后可以粘贴到 web 应用程序中。然后，应用程序处理生成必要的代码，以对应于物理布局的顺序寻址 led。

[Jason]很好地解释了该工具是如何工作的，并通过彩虹动画演示了它如何与类似蝴蝶结的蛇形布局一起工作。该工具甚至可以提供布局的视觉预览，以便您可以验证您输入的内容是否有意义。

这是一个很棒的工具，我们最近看到它在[极客 Faye 的优秀项链项目中投入使用。休息后的视频。

> 我的 LED 映射应用程序现在支持渐变调色板！还为样本模式提供了可交互编辑的伪 [#FastLED](https://twitter.com/hashtag/FastLED?src=hash&ref_src=twsrc%5Etfw) 代码。支持网格布局、XY 坐标、 [#Pixelblaze](https://twitter.com/hashtag/Pixelblaze?src=hash&ref_src=twsrc%5Etfw) 地图等之间的转换。
> App:[https://t.co/nxycSh9hig](https://t.co/nxycSh9hig)
> 代码:[https://t.co/riPnnRhFSF](https://t.co/riPnnRhFSF)pic.twitter.com/gXgTS0L6UN
> 
> —杰森·库恩(@ Jason Coon _)[2022 年 2 月 10 日](https://twitter.com/jasoncoon_/status/1491579670348894215?ref_src=twsrc%5Etfw)