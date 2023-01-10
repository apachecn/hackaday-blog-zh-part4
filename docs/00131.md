# 没有希德的悲伤？这非常接近

> 原文：<https://hackaday.com/2018/07/24/sad-without-a-sid-this-comes-pretty-close/>

MOS Technologies 6851，俗称 SID，是 20 世纪 80 年代早期的传奇声音合成器集成电路，最著名的是为 Commodore 64 家用计算机提供了制造噪声的能力。当时，它明显优于竞争对手的机器，成为当今 chiptune 和演示场景艺术家的热门选择。

然而，对于现代的 SID-jockey 来说，这种芯片已经停产四分之一世纪，因此供不应求。仿真是一种选择，但对于原始硬件的所有者来说用处不大，所以幸运的是[Petros Kokotis]已经使用 Teensy 3.6 生产了 SID 替代品。

操作非常简单，Teensy 通过一些电平转换器为主机微计算机提供所有必需的 SID 数据线，并使用[Frank Boesing]的 [ReSID 库](https://github.com/FrankBoesing/Teensy-reSID)来完成作为 SID 的繁重工作。[你可以从 GitHub 库](https://github.com/kokotisp/6581-SID-teensy)下载代码，他发布了一个视频，我们把它放在休息时间下面，展示了一个原型和一个真实的 Commodore 64 的运行。由于手机摄像头从一个非常小的扬声器录音，音频质量并不出色，但尽管如此，它有真实的东西。

这不是我们在这里见到的第一只希德。用一个做一个[MIDI 合成器怎么样？](https://hackaday.com/2012/10/18/creating-a-midi-synth-from-a-commodore-sid/)

 [https://www.youtube.com/embed/6Os3Q98QT08?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/6Os3Q98QT08?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

