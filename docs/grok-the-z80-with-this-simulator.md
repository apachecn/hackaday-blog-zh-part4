# 用这个模拟器搜索 Z80

> 原文：<https://hackaday.com/2020/07/20/grok-the-z80-with-this-simulator/>

我们中的许多人都会在某个时候遇到 Z80 微处理器，无论我们是为它编写了裸机程序，还是只是尝试使用它在游戏系统上消灭一些入侵者。像那个时代的所有处理器一样，它有一个相对简单和容易理解的内部框图，所以读者也很有可能知道它是如何工作的。但是有谁知道它到底是如何工作的吗，一直到栅极、晶体管和网络层面？[Goran]知道，因为他写了一个 [Z80 网表模拟器](https://baltazarstudios.com/z80explorer/)，允许在检查芯片及其信号的同时运行代码。它不是特别快，在相当高端的 PC 上运行时达到了 2.3kHz 的时钟速度，但我们猜测需要运行 Z80 代码而不是学习的读者无论如何都会使用真实的东西。

我们在 break 下面放了一个软件运行的视频，我们可以看到它将是一个迷人的工具，即使对于不是专门的逆向工程师的人来说也是如此。如果你习惯于把它作为一个黑匣子，那么能够在处理器运行时调出处理器内部的逻辑分析仪视图确实令人震惊，并且让逻辑图唾手可得而不是弄不清单个晶体管确实提供了一个了解正在发生什么的窗口。

这并不是唯一一个这样的模拟器，过去我们在讲述[怪物 6502](https://hackaday.com/2016/05/16/a-dis-integrated-6502/) 的时候提到过 [Visual6502](http://visual6502.org/) 。

 [https://www.youtube.com/embed/_dyngzTEnvw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/_dyngzTEnvw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

