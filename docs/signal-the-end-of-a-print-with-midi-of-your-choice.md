# 用您选取的 MIDI 来表示打印结束

> 原文：<https://hackaday.com/2020/04/25/signal-the-end-of-a-print-with-midi-of-your-choice/>

每一个 3D 打印的结尾都应该是一个胜利的时刻，值得一首主题曲。[FuseBox2R]决定让它成为现实，并编写了将 [MIDI 轨道转换为 g 代码](https://www.reddit.com/r/3Dprinting/comments/g3lqm2/i_wrote_a_program_that_converts_midi_files_to/fnrzp7p/?context=3)的工具，该工具使用 3D 打印机上的蜂鸣器。

该工具安装在 [GitHub](https://github.com/alexyu132/midi-m300) 上，并使用 Marlin 和其他一些 3D 打印机固件包中提供的 M300 扬声器命令。它采用带有内嵌 JavaScript 的静态 HTML 页面的形式，使用 [Tone.js](https://tonejs.github.io/) 框架将 midi 轨道转换为一系列具有适当频率和持续时间参数的扬声器命令。只需添加到您的切片机的 g 代码添加一点香料到您的打印。你也可以用斜坡板和 LCD 来制作一个 MIDI 点唱机，你可能在某个地方积了灰尘。休息后观看视频演示，包括《毁灭战士》主题曲的演唱，当然还有《马里奥兄弟》。

对于更多的隔离项目，你也可以使用你的打印机上的步进电机播放 MIDI，或者如果时间变得太模糊的话，制作一个 T2 日历时钟。

 [https://www.youtube.com/embed/gurSmmTxVug?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/gurSmmTxVug?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

