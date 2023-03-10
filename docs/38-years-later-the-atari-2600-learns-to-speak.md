# 38 年后，雅达利 2600 学会了说话

> 原文：<https://hackaday.com/2020/08/27/38-years-later-the-atari-2600-learns-to-speak/>

早在 20 世纪 80 年代初，让你的计算机产生类似人类语言的东西曾风行一时。对此有几种硬件解决方案，从自动电话系统到视频游戏机，一直到史蒂夫·乔布斯在 1984 年用这个噱头向世界介绍麦金塔电脑，都加入了声音。1982 年，这种合成的基于软件的版本为 Atari 8 位系列计算机发布，从那以后[rossumur]一直想知道它是否能在非常受限的 2600 上运行。

一晃 38 年过去了，他发现答案是肯定的，确实有可能移植类似于 1982 年的软件 Automatic Mouth(或 SAM)完全在 Atari 2600 上运行[，而不需要任何额外的硬件。为了能够将这样一个看似复杂的软件放入微不足道的 128 字节(是的，字节)RAM 中，[rossumur]实际上使用了一个创作工具来预先计算音位变体，并只将它们存储在 ROM 中。这样，2600 不能单独将文本转换成音素，但有足够的空间用于音位变体，音位变体被转换成声音，大约两分钟的讲话可以装入一个墨盒。至于他为什么遇到麻烦，我们引用作者自己的话:“因为在 1977 年的游戏机上用 1982 年的语音合成技术创建数字脏话正是我们现在需要的。”](https://youtu.be/abL_H784Vck)

为了这个项目，[rossumur]已经写了一篇关于语音合成的非常有趣的文章来解释这里使用的 SAM 引擎。这也不是他第一次上网站，总是在不合适的地方塞进软件，比如[的类似“网飞”的流媒体服务](https://hackaday.com/2020/08/11/espflix-brings-streaming-video-to-the-world-of-microcontrollers/)，或者[的 8 位控制台仿真器](https://hackaday.com/2020/06/09/run-your-favorite-8-bit-games-on-an-esp32/)，这两个软件都只在一个 ESP32 微控制器上运行。休息之后看看这个。

 [https://www.youtube.com/embed/abL_H784Vck?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/abL_H784Vck?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

