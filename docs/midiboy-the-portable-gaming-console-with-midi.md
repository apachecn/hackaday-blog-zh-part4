# Midiboy，带 MIDI 的便携式游戏机

> 原文：<https://hackaday.com/2019/07/06/midiboy-the-portable-gaming-console-with-midi/>

ArduBoy 是一个非常小的游戏控制台，也非常简单。它只是一个小型、廉价的单色有机发光二极管显示器，一个带有 Arduino 衍生固件的微控制器和几个按钮。就是这样，但有了这些简单的成分，ArduBoy 周围的社区已经创建了一个可行的游戏平台。它现在有墨盒，一个版本有一个曲柄。现在，MIDIboy 正将类似 ArduBoy 的东西带入电子音乐世界。

在 MIDIboy 里面是你从任何对 ArduBoy 原理图的回顾中所期待的。有六个按钮，一个扬声器，一个 USB 端口和一个 SPI 有机发光二极管显示器。除此之外，还有两个大的 chonkin' DIN-5 端口用于 MIDI 输入和 MIDI 输出，是的，MIDI 输入端口有一个光隔离器。

至于你可以用一个连接到 MIDI 的小游戏控制台做什么，已经有几个选择应用程序了——显然，MIDI 和弦应用程序创建和弦，MIDImon sketch 是一个 MIDI 监视器。有一些 MIDI 合成器的控制器，当然这个设备是完全开源的。如果你曾经想要一个 DIY 控制器来控制你最喜欢的 MIDI 合成器，这就是你所需要的。

如果一个带 MIDI 的 ArduBoy 听起来不令人兴奋，[就去看看小声音 DJ](https://www.littlesounddj.com/lsd/index.php) 。这是一款 Game Boy 卡带，可将您的旧砖块游戏机变成音乐制作工作站。是的，这听起来很棒，有 MIDI 端口的袖珍游戏机有很大的潜力。