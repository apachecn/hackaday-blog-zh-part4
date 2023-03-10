# 树莓 Pi Pico 的 VGA 库

> 原文：<https://hackaday.com/2021/06/11/vga-library-for-the-raspberry-pi-pico/>

[Miroslav Nemecek]通过他的 PicoVGA 项目真正推动了 Pico 的极限，该项目包含了数量惊人的功能。他用这个库的主要目标是运行复古游戏，这些游戏可以在 Pico 有限的 RAM 和处理能力范围内运行，但下面的演示视频显示了广泛的潜在应用。

该库提供了一系列功能，包括帧缓冲、子画面、叠加和高达 1280×960 的 NTSC 或 PAL 定时分辨率。封装中还包括一个 PWM 驱动的音频输出通道。他的库充分利用了可编程 I/O 模块的功能，并使用了专用于视频处理的第二个内核。但是，如果小心，第二个内核可以在某些情况下执行应用任务。VGA 模拟输出信号由电阻梯提供，像素颜色为 8 位 R3G3B2 格式。需要澄清的是，[Miroslav]在某一方面确实有点作弊——他将处理器超频到 270 MHz，以满足某些分辨率的时序要求。

[Miroslav]在 Windows 上使用 ARM-GCC 开发了这些工具，但是他缺乏构建 Linux 的经验。他欢迎任何熟悉 Linux 的人在这方面提供帮助。请继续关注——未来可能会有更多来自[Miroslav]的消息。他指出 PicoVGA 库是作为一个仍在开发中的复古游戏电脑项目的一部分而创建的。我们期待在它发布的时候听到更多关于它的消息。

几周前，我们写了一篇由[Nick Bild]撰写的 Pico 的单色 VGA 版 Pong。看到这些探索 Pico 能力极限的项目令人兴奋。你有没有看到任何突破极限的微微应用？请在下面的评论中告诉我们。感谢[Pavel Krivanek]将此项目发送到我们的举报热线。

 [https://www.youtube.com/embed/wX1IPa3Q0LU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/wX1IPa3Q0LU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

