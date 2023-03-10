# Wordle 逆向工程和自动求解

> 原文：<https://hackaday.com/2022/02/08/wordle-reverse-engineering-and-automated-solving/>

![](img/311ed68c9b5fa0bb3eb40c0a4aea05c0.png)

Simplified Absurdle decision tree for a single letter guess from a set of three possible options

我们不知道你，但我们对在线益智时尚有着复杂的感情。一方面，它们是帮助保持敏锐的好工具，但它们只是无处不在。最新的社交媒体驱动的时尚，Wordle，对我们来说可能有点太流行了，社交媒体时间线塞满了关于这个东西的更新。[埃德·洛卡德]对朋友们不断发表关于“今日世界”的帖子感到有点恼火，希望他们能回去张贴他们的狗的照片，任何有自尊的黑客都会这样做，[写了一个 python 脚本来自动解决世界谜题](https://medium.com/@l0c4rd/how-i-broke-wordle-solved-absurdle-and-lost-all-my-friends-e97f064aded9)，试图让他们停止张贴，但可能是徒劳的。

实际上，[Ed]更感兴趣的是为一个相关的游戏构建一个解算器， [Absurdle](https://qntm.org/absurdle) ，它被描述为 Wordle 的一个对抗性变种。这实际上并不选择一个单词，而是使用您目前的猜测来缩小一个可能单词的大池，让您猜测更长时间。这是非常卑鄙的。总之，[Ed]想出了一个叫做[Pyrdle](https://github.com/L0C4RD/Pyrdle)(GitHub 项目)的工具，它本质上是 Absurdle 的命令版本，也有能力解决 Wordle 的副产品。原来 Wordle 的 JS 实现包含了客户端所有可能的单词列表，所以答案已经在浏览器中了。这个项目真正有趣的部分是自动解决有大量潜在解决方案的难题的方法。这是一篇有趣的文章，比阅读另一篇 Wordle 帖子要有趣得多。

最后一点:如果你对这个不感兴趣，爱 Wordle，并且不能满足，你可能想安装[brackendawson]的滑稽标题(command)[*not foundle*](https://github.com/brackendawson/notfoundle)shell 处理程序，为你的命令行失误提供一些令人费解的反馈。不管怎样，这让我们很开心。

益智项目偶尔会出现在这些页面上。这里是[年度圣诞 GCHQ 拼图](https://hackaday.com/2021/12/13/pit-your-wits-against-british-spooks/)，如果你对物理拼图更感兴趣，有一个电子焦点(并且可以焊接)看看 [DEF CON 29 拼图徽章](https://hackaday.com/2021/08/02/andxors-def-con-29-electronic-badge-is-an-assembly-puzzle/)！