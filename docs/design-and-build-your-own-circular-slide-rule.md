# 设计并制作你自己的圆形计算尺

> 原文：<https://hackaday.com/2021/09/25/design-and-build-your-own-circular-slide-rule/>

你必须真正喜欢计算尺，才能建立自己的计算尺，包括必要的艺术品。显然[迪伦·菲恩]是一个大粉丝，基于这个项目，他几个月前就开始工作了。其结果是一套算法，自动生成过去计算尺上常见的大部分刻度。例如:

```
K       Cubic scale, x^3
A,B     Squared scale, x^2
C,D     Basic scale, x
CI,DI   Inverted scale, 1/x
CF,DF   Folded scale, x*pi
LLn     Log-log scales, e^a*x
LL0n    Log-log scales, e^-a*x
L       Log scale, log10(x), linear
S       Sine and cosines scale, sin(x)
T       Tangent scale, tan(x)

```

如果您曾经尝试过使用计算机程序手动绘制轴——尝试自动设置合理的刻度线、网格和标签——您会意识到这是一个不小的问题。[Dylan]自下而上地解决问题，开发了几个协同工作的效用函数，以迭代地构建每个规模。他说，这种方法的一个优点是，你可以非常容易地建立几乎任何你想要的规模。我们将相信他的话，因为这个项目对于普通程序员来说并不容易理解。正如[迪伦]所说:

> 目前它仍然是一个没有文档的库，并且是用一种叫做 Haskell 的相对晦涩的语言编写的，所以它真的只是为特别有决心的人准备的。

该项目[发布在他的 GitHub 库](https://github.com/dylan-thinnes/slide-rules-generator)上，并且提供了样品秤和演示程序。如果没有晦涩难懂的语言知识，并且只是稍微下定决心，至少可以生成一些样本——只需下载 Haskell 环境、一些依赖项，并克隆[Dylan]的存储库。输出是一个 SVG 文件，可以缩放到任何所需的大小。在[这篇后续的 Reddit 帖子](https://old.reddit.com/r/Sliderules/comments/onk9tk/a_homemade_slide_rule_using_a_laser_cutter_for/)中，他讨论了主要照片中所示的丙烯酸圆形计算尺的制作技术。

使用预先生成的艺术作品制作自己的计算尺总是可行的——例如，[计算尺博物馆网站](https://www.sliderulemuseum.com/SR_Scales.htm)提供了大量图形格式的各种标尺。但是如果你想做一个定制的秤，或者做一个米长的秤，看看[迪伦]的项目，试一试。关于制作计算尺的另一个例子，请看我们去年报道过的[这个项目](https://hackaday.com/2020/11/11/homebrew-slide-rule-gets-back-to-mathematical-basics/)。