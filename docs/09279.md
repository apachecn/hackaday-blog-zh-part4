# Arduino 合成器上的 12 音符复调

> 原文：<https://hackaday.com/2021/02/19/12-note-polyphony-on-an-arduino-synth/>

当合成器在 20 世纪中期首次出现时，许多都是单声道乐器，一次只能产生一个音高。这是一个主要的限制，随着时间的推移，复音合成器开始涌入现场，极大地扩展了性能的可能性。[Kevin]决定构建自己的复音合成器，[但他远没有走捷径，而是围绕 Arduino Uno 构建的——这不是一个以音乐能力而闻名的平台！](https://diyelectromusic.wordpress.com/2021/02/05/arduino-tone-polyphony/)

[Kevin]的构建管理 12 个音符的复调，这对于处于 Arduino Uno 核心的 ATmega328 来说是一个令人印象深刻的壮举。它是通过在一个定时器上以稳定的速率运行一个中断，并实现 12 个计数器，每个音符一个。当计数器溢出时，数字 IO 引脚翻转。这将在 IO 引脚上输出特定音高的方波，产生给定音符。12 个数字 IO 引脚的输出通过一个简单的电阻排列混合在一起，产生一个基本的方波合成器。调优并不完美，但[Kevin]指出了一些可以改进的方法。

[凯文]一直在增加功能，通过 MIDI 、[扩展简单的 synth](https://diyelectromusic.wordpress.com/2021/02/14/arduino-tone-polyphony-part-4/) [到几个八度音阶，同时还建立了一个小的触觉按钮键盘。](https://diyelectromusic.wordpress.com/2021/02/10/arduino-tone-polyphony-part-3/)这是一个通向基础合成和音乐电子学的伟大大门，我们相信[凯文]在这个过程中学到了很多。我们以前也见过其他的微控制器合成器，[就像这个装在 MIDI 插头](https://hackaday.com/2016/03/30/the-attiny-midi-plug-synth/)里的小装置。休息后的视频。

 [https://www.youtube.com/embed/slalpoarabI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/slalpoarabI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

