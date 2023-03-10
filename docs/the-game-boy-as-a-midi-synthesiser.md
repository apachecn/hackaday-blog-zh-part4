# 作为 midi 合成器的游戏男孩

> 原文：<https://hackaday.com/2020/08/05/the-game-boy-as-a-midi-synthesiser/>

在 chiptune 音乐的世界里，有许多平台可供选择，每个平台都有自己独特的声音风格。Game Boy 拥有一批特殊的追随者，但它与一些当代平台的不同之处在于，它在处理器所在的硅片上内置了一个定制的声音芯片。你不能打开一个游戏男孩，拿出你自己的 synth 项目的声音芯片，相反，你必须通过游戏男孩的 Z80 处理器与它交谈。这是[Adil Soubki]非常了解的事情，因为他已经完成了一个项目，将手持控制台变成 MIDI 合成器。

Game Boy 是为玩游戏而设计的，而不是作为开发者的玩具，所以它并没有为黑客铺上红地毯。他通过将其内存地址映射的一部分映射到 Teensy 微控制器板上的引脚，并运行一些 Game Boy 代码来读取那里的值，并使用它们来配置声音硬件，从而进入了控制台的皮肤。Teensy 处理 MIDI 和这些字节值之间的转换，将整个变成 MIDI 合成器。这是一个成功的技术，正如我们在下面的视频中看到的。最棒的是，[代码可用](https://bitbucket.org/adilsoubki/gbsynth/src/medium-post-1/)，所以你可以自己试一试。

我们之前在 Hackaday 展示过 Game Boy synths，但通常他们是更传统的种类。

 [https://www.youtube.com/embed/Zlq3IYozDf0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Zlq3IYozDf0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

