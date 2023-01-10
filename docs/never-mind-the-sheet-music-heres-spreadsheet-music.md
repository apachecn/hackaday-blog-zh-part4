# 别管乐谱了，这是电子表格音乐

> 原文：<https://hackaday.com/2019/02/02/never-mind-the-sheet-music-heres-spreadsheet-music/>

没有什么比电子表格软件更能体现摇滚明星音乐家的生活方式了。好吧，我们可能在那句话里混淆了一点词序，但是总会有 Python 来增加一些真实性。毕竟，如果我们看看 MIDI 音序器的基本概念，我们实际上有一排时间间隔步长，根据用户界面，可以是虚拟或实际的音高列或单个乐器。从纯技术的角度来看，电子表格之类的东西在这里会做得很好。

被这个想法逗乐了，[Maxime]写了一个处理 CSV 文件的 Python 音序器，它可以与硬件和软件 MIDI 合成器一起工作。作为 Python，大部分细节都是在外部模块中实现的，这使得[的代码](https://gist.github.com/maximecb/f440c1db489177c1037ec4f158cf5e4f)相当紧凑，易于理解，因为它支持最常见音阶的鼓和旋律轨道。如果你想试一试，你需要的只是 [`python-rtmidi`](https://pypi.org/project/python-rtmidi/) 和 [`mido`](https://mido.readthedocs.io/en/latest/) 模块，你应该可以开始了。

然而，如果你不喜欢电子表格，[Maxime]也有一个基于浏览器的音序器项目，集成了合成器正在进行中，它的前一个版本[也可以在 GitHub](https://github.com/maximecb/MusicToy)上获得。如果软件不适合你，而你更喜欢动手体验，不要担心，MIDI 音序器似乎是一个可靠的灵感来源——无论它们是内置在古代收银机中的，完全由木头制成的，还是仅仅由*制成的[。](https://hackaday.com/2017/04/13/hackaday-prize-entry-zappotron-super-sequencer/)*

 *[https://www.youtube.com/embed/LQOFiC6YIvo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/LQOFiC6YIvo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

*