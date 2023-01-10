# Apple II 上的 NES 开发是什么样子的

> 原文：<https://hackaday.com/2021/05/20/what-nes-development-looks-like-on-the-apple-ii/>

如今，如果你想为最初的任天堂娱乐系统编写游戏代码，只需下载一个汇编程序，启动记事本，在各种仿真器中运行你编写的 rom 即可。在 20 世纪 80 年代，这些东西都不存在，过程稍微复杂一点——[正如下面嵌入的视频中的[Tyler Barnes]](https://www.youtube.com/watch?v=kyN9BZiKqJQ) 所展示的。

[Tyler]已经整理了一个 40 分钟的指南，介绍如何在 NES 上使用正确的硬件进入“Hello World”，或者更准确地说，一个简单的粉红色屏幕。他首先格式化一些软盘，并在 Apple IIe 上快速编写一些基本的汇编代码，这些代码通过 6502 的 Merlin 汇编程序运行。这特别方便，因为 Apple II 系列和 NES 都运行相同的 CPU。从那以后，就可以使用一个独立的 EPROM 编程器来验证一些适当的日期编码芯片是空的，然后将它们编程到 Apple II 的特殊附加卡中。从那里，EPROMs 被装载到定制的带有芯片插座的手推车上，在那里它可以被插入到 NES 中进行测试。

这是一个乏味的过程，仅仅是编程方面的事情就需要 10 到 20 分钟的时间，一路上有一些复杂的步骤。虽然可能会有一些当年工作室使用的效率增益，但很明显，这个时代的开发是一个慢得多的过程。

当然，如果几代人之后你更喜欢你的任天堂自制游戏，可以考虑玩任天堂 64 。休息后的视频。

 [https://www.youtube.com/embed/kyN9BZiKqJQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/kyN9BZiKqJQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



【感谢 Alex McAlpine 的提示！]