# 播放那台时髦的 3D 打印机…

> 原文：<https://hackaday.com/2020/01/19/play-that-funky-3d-printer/>

人类的大脑天生就喜欢音乐。科学家认为最古老的乐器是笛子，可以追溯到 67，000 到 37，000 年前。尽管我们假设人们在那之前很久就在敲打木头或大腿，或者敲打两块石头。几乎任何东西都可以成为乐器。一个典型的例子:[elifer5000]走进一个房间，里面有许多正在运行的 3D 打印机，并认为它似乎很有音乐感。接下来你知道，他利用 3D 打印机作为 MIDI 乐器。

在一次黑客马拉松上，他发现了一些将 MIDI 文件转换成 GCode 的软件。唯一的问题是一台普通的打印机有三个轴，因此一次只能(最多)生产三张钞票。这个问题的显而易见的答案是使用更多的打印机，这就是他所做的，你可以在下面看到。

显然，步进电机移动的速度与它发出的音调成正比。当然，在给定速度下行进的距离对应于音调持续的时间。鉴于此，计算出音符的参数是一个非常简单的数学问题。

普通打印机的 Z 轴速度较慢，因此最终产品在每台打印机上仅使用 X 轴和 Y 轴。这意味着你甚至可以使用数控机床或绘图仪作为打印机的一部分。

当试图实时处理 MIDI 文件时，出现了一个问题。当你开始一个音符时，你不知道它会持续多久。只有当音符停止时，你才会知道它已经结束。当你记得当你第一次按下一个键时，MIDI 键盘不知道你会按多久，这是有道理的。该代码使用一个 50 毫秒的小“微音符”并播放它，直到停止信号到达。

Python 代码需要一点校准，因为每台打印机都有点不同。正如你所料，结果有点电子化，但足够令人愉快，而且肯定胜过两块石头。我们以前见过在软驱和硬盘上播放音乐。或者，你可以反其道而行之，使用[硬盘作为麦克风](https://hackaday.com/2019/03/13/hackers-turn-hard-drive-into-microphone-that-can-listen-in-on-your-computers-fan-whine/)。

 [https://www.youtube.com/embed/mluO7YGOsOs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/mluO7YGOsOs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

