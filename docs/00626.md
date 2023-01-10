# 少即是多:一平方英寸的微矩阵显示器

> 原文：<https://hackaday.com/2018/09/12/less-is-more-a-micromatrix-display-in-a-square-inch/>

在你的客厅里，大显示屏是你想要的。但是在嵌入式项目中，通常越少越好。我们认为[bobricius]会同意，因为他在我们的平方英寸挑战赛中提交了一个[微型 4×5 LED 显示屏](https://hackaday.io/project/18635-standalone-led-micromatrix-display)。该板具有一个 ATtiny CPU 和 20 个 SMD LEDs，呈漂亮的网格状。你可以在下面的视频中看到他们的动作，滚动到一些迪斯科音乐。

CPU 中有足够的空间来存储更大的文本字符串——闪存的空间刚刚超过 10%。如果你想改变什么，一个侧面安装的小接头可以很容易地对芯片进行编程。

为了节省引脚，显示器使用[查理多路复用](https://hackaday.com/2008/12/03/intro-to-charlieplexing/)，他以前使用的相同技术用 11 个 I/O 引脚驱动 [110 个引脚。一般来说，对于给定数量的 I/O 引脚(称之为 N)，您可以驱动 N -N 个 led。在这种情况下，他用 5 条线驱动 20 个 led。当然，发光二极管不会一直亮着，但芯片驱动它们的速度足够快，以至于你不知道它们之间的区别。](https://hackaday.com/2017/04/04/hackaday-prize-entry-micro-matrix-charlieplexed-displays/)

我们不得不承认，剩下这么多代码，我们想知道你是否能做一些有趣的事情，允许它们通过一些串行协议来控制，甚至可能将它们菊花链在一起，以制作更大的显示器。但我们认为他已经筋疲力尽了。

* * *

 [https://www.youtube.com/embed/GU3U1sHmEaM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/GU3U1sHmEaM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

