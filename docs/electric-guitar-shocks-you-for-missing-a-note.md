# 电吉他让你震惊，因为你错过了一个音符

> 原文：<https://hackaday.com/2022/10/06/electric-guitar-shocks-you-for-missing-a-note/>

Rocksmith 是一款流行的视频游戏，它的工作方式类似于*吉他英雄、*，但使用的是一把真正的吉他。你必须弹得好，打对音符，否则比赛会扣分。[Lightwing]将赌注提高了一个档次，增加了一个系统，每当玩家[失败时，这个系统都会让玩家震惊。](https://hackaday.io/project/187530-electrified-guitar-tazer-guitar)

为了实现这一点，有必要检测演奏者何时错过了一个音符。最初的尝试包括使用张量流人工智能从屏幕上检测游戏状态，但这并不可靠。相反，游戏的内存被读取，以实现检测。当玩家错过一个音符时，内存的某一部分发生变化，一个脚本读取游戏状态的变化。然后，它向 Arduino 发送信号，触发眩晕枪的发射按钮，电击手持吉他的玩家。

正如你所料，这个项目的文档包括一个视频，其中涉及到当[Lightwing]犯错误时的大量无端电击。公平的警告——当眩晕枪开火时，有很多丰富多彩的语言。一般来说，强烈的震惊会以尖叫、吉他掉落和太多的恐惧而结束。

这很痛苦，它可能不是学习吉他的有用教学工具。我们以前也见过类似的令人震惊的构建，比如这个简单的连线游戏。

 [https://www.youtube.com/embed/jnBYp512dPM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/jnBYp512dPM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

