# 由 RP2040 提供的 Breakbeats

> 原文：<https://hackaday.com/2022/02/09/breakbeats-courtesy-of-the-rp2040/>

虽然一个人经常完整地听歌曲或专辑，但有时你只想放下一个简单的节拍。[todbot]的最新项目[承诺做到这一点。](https://twitter.com/todbot/status/1491222284925022209)

构建依赖于 Raspberry Pi Pico 或任何其他基于 RP2040 的微控制器板，并使用 [CircuitPython 编程。](https://hackaday.com/tag/circuitpython/)PWM 功能用于音频输出，它加载了经典“阿门”中断的不同 WAV 样本。

每一个小节，一个随机的新样本被选择和演奏，改变节拍。更好的是，所有的样本都可以循环，它们有不同的长度，允许它们相互重叠，以增加混合的深度。这很容易设置，因为 CircuitPython 内置了一个 AudioMixer 对象。

那些希望自己动手的人可以在 Github 上找到所有的代码和示例。毕竟，像这样的构建是开始学习处理音频和音乐的一个很好的方式。[我们以前也在这里看过【托德博特】的作品。](https://hackaday.com/2017/03/12/neojoints-make-ws2812-leds-even-more-fun/)休息后的视频。

> 想要 breakbeats 但没有时间？让 [#CircuitPython](https://twitter.com/hashtag/CircuitPython?src=hash&ref_src=twsrc%5Etfw) 在基于 [@Raspberry_Pi](https://twitter.com/Raspberry_Pi?ref_src=twsrc%5Etfw) RP2040 的板上完成这项工作。CirPy 可以轻松地同时播放多个样本。而 RP2040 芯片有 PWM 音频输出。代码跟随 pic.twitter.com/CutQz0bNao
> 
> —托德·库尔特(@托德·博特)[2022 年 2 月 9 日](https://twitter.com/todbot/status/1491222284925022209?ref_src=twsrc%5Etfw)