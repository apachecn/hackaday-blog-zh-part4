# 在朋友的帮助下，Arduino 变成了超级英雄

> 原文：<https://hackaday.com/2021/10/10/arduino-becomes-superhet-with-a-little-help-from-friends/>

收音机总是一个有趣的项目。[Jayakody2000lk]决定他的新[超外差设计](https://www.instructables.com/DIY-Arduino-Superheterodyne-Receiver/)将使用 Arduino，它看起来非常漂亮。该系统有四块板。一个现成的 Arduino、一个 Si5351 时钟发生器板(也是现成的)，以及两个包含 IF 放大器和混频器的定制板。

接收器在 2015 年开始没有 Arduino，在帖子中有一个链接指向最初的设计。使用 Si5351 和 Arduino 取代了原来的本地振荡器，并且还有其他改进。你可以在下面看到一个关于接收器的视频。

调谐是由一个旋转编码器和当前的软件让你从大约 4.75 兆赫调谐到略高于 15.8 兆赫。当然，只要混频器和其他组件能够处理，您可以将 Si5351 转换到它能够处理的任何频率。中频频率通常为 455 kHz。

如果你决定自己做这个，设计文件在 [GitHub](https://github.com/dilshan/arduino-superhet) 上。总的来说，这是一个非常漂亮简洁的设计。自从埃德温·阿姆斯特朗(Edwin Armstrong)的时代(T2)以来，无线电架构的变化如此之小，我们总是感到惊讶。当然，我们有更好的组件，即使[它们不是用于无线电目的](https://hackaday.com/2021/04/19/a-superheterodyne-receiver-with-a-74xx-twist/)。

 [https://www.youtube.com/embed/8Wvycy0YoPc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/8Wvycy0YoPc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

