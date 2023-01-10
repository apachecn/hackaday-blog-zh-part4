# 加快平衡木的速度，降低一些节拍

> 原文：<https://hackaday.com/2018/10/23/racing-the-beam-and-dropping-some-beats/>

雅达利 2600 的核心不是 6502(或者学究用的 6507)，而是 TIA 芯片。这个芯片负责在显示器上绘制图形，控制光束，并对声音生成提供极其有限的支持。我们还没有看到很多将 Atari 2600 用于 chiptunes 的尝试，但这并不意味着它不能做到。[【John Sutley】的 Syndrum 是对 Atari 2600 鼓机的模仿](https://hackaday.io/project/161467-syndrum-an-atari-2600-drum-machine)几乎是一件艺术品。它是木质面板的 Atari 的定制墨盒，也是一个令人印象深刻的输入设备，可以将这个经典的控制台变成一台打击机

雅达利 2600 有没有配备过鼓机拾音器？也许吧。大概不会。[John]最初建立这个项目是为了试验 TIA 芯片，但发现它的音调不如 kazoo。这使得“雅达利合成器”从列表中消失，取而代之的是“雅达利鼓机”。这里有两个关键部分，第一个是重新设计的小行星子弹，用 ZIF 插座取代了 PROM。这使得[John]可以轻松地将新代码烧录到 EEPROM 中，插入插座，然后在 Atari 上运行。所有代码都是用 batari Basic 开发的，这是一种受 Basic 启发的语言。雅达利的 bin 文件。

但是在 Atari 上运行代码只是这个版本的一半。要做一台架子鼓，你需要告诉 Atari 何时播放每种声音。鉴于 Atari 缺乏扩展能力，[John]转向了控制器端口。Syndrum 使用 Arduino Nano 将 DE9 控制器连接器连接到 MIDI 端口。是的，它是真正的 MIDI，在一台机器上，它可能永远也不会自己做 MIDI(尽管我们很乐意看到有人尝试)。

需要一个令人兴奋的黑客视频吗？给你:

 [https://www.youtube.com/embed/rJQEGqaRtjs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/rJQEGqaRtjs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

