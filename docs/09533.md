# 没有(不必要的)延迟的吉他效果

> 原文：<https://hackaday.com/2021/03/15/guitar-effects-with-no-unwanted-delay/>

自从 20 世纪 80 年代发明以来，MIDI 已经成为音乐家和艺术家的一个很好的工具。它允许一种标准的方式将乐器连接到计算机，以便于音乐的录制、编辑和制作。但它也有一些弱点，即如果没有一些专门的设备，信号通过各种连接设备的等待时间很容易变得过高，无法用于现场表演。[正如[Philip Karlsson Gisslow]所阐述的，用正确的设备](https://www.youtube.com/watch?v=Fu0Qsz2h3HE)并不是不可能解决的问题。

他创建的低延迟 MIDI 接口是围绕 Raspberry Pi Pico 构建的。它运行一个由[Philip]创建的名为 MiGiC 的定制库，专门作为 MIDI 到吉他的接口。整个设置包括一个前置放大器，将吉他信号提升至 3.3V，然后馈入 Pi。这是 MIDI 采样完成的地方。从那里，它将信息[发送到 PC](https://en.wikipedia.org/wiki/Digital_audio_workstation), PC 能够快速播放声音，没有明显的延迟。

[Philip]还必须做大量额外的工作来将软件移植到 Pi 上，Pi 缺少 Mac 或 Windows 机器上的原始硬件的许多功能，结果令人印象深刻，特别是在视频的结尾，他使用界面通过他的吉他弹奏架子鼓。虽然 MIDI 对于吉他手来说无疑是一个强大的应用程序，但是我们也看到了圆周率在这个音乐领域的其他用途。

 [https://www.youtube.com/embed/Fu0Qsz2h3HE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Fu0Qsz2h3HE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[乔希]的提示！