# Arduino 驱动 600 字符显示器

> 原文：<https://hackaday.com/2020/02/14/arduino-drives-a-600-character-display/>

[Peterthinks]承认他不是橱柜制造商，所以他的项目使用了大量的热熔胶。他也承认自己不是视频编辑。然而，他的最新视频使用了一些 a MAX7219 来创建一个 [600 字符滚动 LED 标志](https://www.youtube.com/watch?v=5F8OdOKuIxc)。你可以在下面看到一段视频。剧透:不是所有的角色都能一次看到。

该项目的核心是 MAX7219 四合一 LED 显示屏，价格远低于 10 美元。该板有四个 LED 阵列，可显示 8×32 个 LED。MAX7219 通过 10 MHz 串行总线接收 16 位数据字，因此编程非常简单。

MAX 芯片可以解码七段显示器，或者只允许您直接点亮输出，这就是这里的代码所做的。您可以级联芯片，因此可以将多个模块串联在一起。

代码可在[下拉框](https://www.dropbox.com/s/wurm3cryuz4mvjx/600%20character%20scrolling%20text%20code.txt?dl=0)上获得。由于使用了 [Parola](https://github.com/MajicDesigns/MD_Parola) 库和 [MAX72XX](https://github.com/MajicDesigns/MD_MAX72XX) 库，代码非常简单。我们已经看到了许多基于[这种芯片](https://hackaday.com/2019/11/03/rise-and-shine-with-this-japanese-inspired-clock/)的项目。有些用途[相当新颖](https://hackaday.com/2019/09/22/a-hard-rocking-arduino-visualization-shield/)。

 [https://www.youtube.com/embed/5F8OdOKuIxc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/5F8OdOKuIxc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

