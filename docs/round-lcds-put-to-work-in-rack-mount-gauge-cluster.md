# 圆形液晶显示器在机架安装仪表组中投入使用

> 原文：<https://hackaday.com/2022/05/13/round-lcds-put-to-work-in-rack-mount-gauge-cluster/>

像你们中的许多人一样，我们对价格合理的圆形液晶面板所提供的可能性很感兴趣。但是，除了为智能手表而设计之外，为这种非传统显示器找到合适的应用并不容易。数字“蒸汽表”是人们首先想到的想法之一，所以[也许毫不奇怪这就是【汤姆·道德】进行他的项目](https://hackaday.io/project/185180-rack-mount-midi-meters)的方向。但是，他决定全力以赴，将其中八个安装在 1U 的机架安装单元中，而不仅仅是一两个仪表。

你要八个模拟压力计做什么？难倒我们了，但那不是我们的部门。现在[汤姆]有了一整排指标，可以用来显示他喜欢关注的任何东西。事实上，该设备实际上是通过 MIDI 控制的，这可能为我们提供了一个线索，即有一个音乐组件在起作用(没有双关语的意思)，但是，这不是我们第一次看到 MIDI 被简单地用作一种方便且受良好支持的同步小工具的方式。

[![](img/1c2cedbf2a7ea26a6bdcd831baba5bfa.png)](https://hackaday.com/wp-content/uploads/2022/05/lcdrack_detail2.jpg)

除了八个 240 x 240 像素面板之外，该单元还具有一个 Teensy 4.0、一些电平转换器和一个 74HC138，后者用于选择微控制器要与之通信的显示器。在软件方面，他使用 Arduino 环境，其中一些 PNG 解压缩例程来自[Larry Bank]，图形代码来自[moonournation]。仪表的背景图像显然是一张许可的库存照片，这可能看起来有点奢侈，但我们不能否认最终的结果看起来非常逼真。

就在去年，我们[报道了使用圆形液晶显示器](https://hackaday.com/2021/12/11/getting-familiar-with-round-displays/)的初级读本，我们已经看到一些[有进取心的黑客在定制智能手表](https://hackaday.com/2019/05/01/scratch-built-smartwatch-looks-pretty-darn-sharp-with-3d-printed-case-and-round-lcd/)中使用它们。无论你是患了恐麦症，还是厌倦了被限制在你的小工具中同样无聊的显示，看到社区接受这项新技术都是令人兴奋的。