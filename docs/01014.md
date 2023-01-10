# wave table General MIDI For every one

> 原文：<https://hackaday.com/2018/10/30/wavetable-general-midi-for-everyone/>

用电脑创作音乐的方法只有这么多，目前最流行的方法是 MIDI。它已经存在了三十五年，你不会无缘无故地成为一个几十年前的标准。也就是说，将 MIDI 转换成音频是一件痛苦的事情，但 Hackaday 奖的乐器挑战赛中的这个项目让这变得很容易。是一个 Fluxamasynth 模块把 MIDI 变成你能听到的东西。

这种构建的关键是一个单一的芯片，它根据 128 种通用 MIDI 声音接收 MIDI 数据并输出音频。这听起来可能没什么，但是如果你曾经试图将 MIDI 转换成声音，你会发现你的选择是有限的。有一种芯片可以做到这一点，并且很容易获得:来自 Dream Sound Synthesis 的 SAM2695。这种芯片最初是为廉价的玩具键盘设计的，但如果你有芯片，你可以用它做任何事情。

Fluxamasynth 模块的灵感来自最初的 Fluxamasynth ，这是一个 Arduino 屏蔽，基本上是 SAM 芯片的分线板。有一个 MIDI 输入，一个 1/8”的输出插孔，没有其他的。Fluxamasynth 模块通过添加更多支持来扩展功能，包括立体声输出、混响、合唱、法兰和延迟效果，并深入挖掘可配置的参数进行调谐。

硬件基本上是 Arduino、Raspberry Pi 和 ESP32 的音频设备，并允许通过代码生成音乐。你可以在下面的视频中看到这个项目的例子。

[https://player.vimeo.com/video/234331540](https://player.vimeo.com/video/234331540)

The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)