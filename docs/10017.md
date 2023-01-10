# 小范围的复调音乐

> 原文：<https://hackaday.com/2021/05/09/polyphony-on-a-tiny-scale/>

老读者可能还记得唱针，这是一种小型电池供电的电子琴，使用导电 PCB 板和唱针来创作音符。这些乐器中简单的多谐振荡器使它们成为单声道，但在 2021 年，我们可以做得更好！[Sjm4306]在 PCB 风琴方面更进一步，[制造了一种拥有四音符复调的电容式触摸乐器](https://hackaday.io/project/178953-polyphonic-touch-pcb-piano)。

它的核心是 ATmega328p，其软件有四个音调发生器，每个发生器出现在不同的引脚上。这些信号通过一组 100ω电阻相加，并馈入一个微型扬声器。电力来自 CR2032 锂电池，他指出，电压越高，音量越大。

完整的故事在休息时间下面的视频中有详细描述，还有一点四音符的复调动作。我们猜测，当连接到混响单元时，这种乐器听起来会很棒。

 [https://www.youtube.com/embed/3xUH_vCHk9A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/3xUH_vCHk9A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

