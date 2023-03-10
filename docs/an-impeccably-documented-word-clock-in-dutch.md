# 一个无可挑剔的荷兰语单词时钟

> 原文：<https://hackaday.com/2022/07/18/an-impeccably-documented-word-clock-in-dutch/>

[马腾·彭宁斯]分享了一个单词时钟项目，但不是普通的那种。首先，这款时钟是业余爱好者可用的 3D 打印技术的一个闪亮演示，由于双挤出机打印机，它内嵌了用透明细丝打印字母的光导。对于一个单词时钟来说，它出奇的小——事实上，它使用了 8×8 可寻址 LED 矩阵，单词以不同的颜色显示。如果你想建造一个新颖的单词钟，你已经准备好了——[ Maarten]讲述了这个项目的所有故事，并提供了一个关于设计各个方面的见解宝库！

最初设置 8×8 的限制是因为他想使用低成本的 MAX7219 8×8 LED 矩阵模块作为时钟的基础。令人欣慰的是，在荷兰语中，时间可以用更短的词来表达——尽管如此，它必须被限制在 5 分钟的间隔内。[必须花费额外的精力](https://github.com/maarten-pennings/WordClock#2-model-1)来设计布局— [Maarten]提到他的朋友写了一个求解器，找到了一种方法来将一些单词放在布局的对角线上。在某个时候，他从 LED 转向了 Neopixels，并深入研究了可寻址 LED 技术。例如，他演示了新像素功率测量和电流消耗计算。这表明，当通过外部仪表测量时，计算结果确实与时钟的实际消耗相匹配。

在最好的黑客传统中，所有的源文件[都在 Github](https://github.com/maarten-pennings/WordClock) 上——如果你想象自己是一个荷兰单词时钟，你可以很容易地构建[Maarten]的设计！他在[的自述文件](https://github.com/maarten-pennings/WordClock/blob/master/README.md)中提供了关于建造这个时钟的详细说明，包括闪光和配置教程、完整的接线图和焊接指南。制造级的大量构建信息不会让您瞎猜。他还添加了相当数量的动画，在时钟精度验证方面投入了大量精力，甚至研究了一些 Neopixel 协议细节。总而言之，我们的黑客在接受约束的同时，把所有的能力都投入进去了。这让我们想起了一年前我们报道过的同样有据可查的[触觉单词时钟](https://hackaday.com/2021/03/30/the-word-clock-you-can-feel/)——也来看看吧！

 [https://www.youtube.com/embed/8YMuuo80cz0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/8YMuuo80cz0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

