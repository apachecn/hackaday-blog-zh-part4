# 迷笛竖琴看起来很锋利

> 原文：<https://hackaday.com/2019/08/17/midi-harp-looks-pretty-sharp/>

[朱利安]是那些用时间投入而不是金钱来表达他的爱的酷爸爸之一。他的女儿弹竖琴，你不会相信音乐会竖琴的价格。即使是便宜的也要几千美元。很自然地，他决定从头开始给她做一把 MIDI 音乐会竖琴。

这项大胆的工作正在进行中，在每根弦上使用应变仪和 AD620 放大器来检测弹拨时的张力。这些放大器连接到 Arduino，每九根弦一个 Arduino。Arduinos 通过 USB 向 Raspberry Pi 发送 MIDI 事件，Raspberry Pi 运行开放式 synth 平台 Zynthian 和 Pianoteq。

竖琴上挂着涂有银色的吉他弦，因为他也想要电容式触摸支持。但是由于速度和可靠性问题，他放弃了这个计划。休息时间过后，请观看一段简短的演示视频。

[朱利安]使用弦乐，因为他想锚定触感的竖琴手。但是你是对的。许多 MIDI 竖琴使用激光。

 [https://www.youtube.com/embed/OkyQwXfiDy0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/OkyQwXfiDy0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

