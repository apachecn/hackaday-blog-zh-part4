# 带 MIDI 的闪烁 led，逐个音符

> 原文：<https://hackaday.com/2019/07/17/flashing-leds-with-midi-note-by-note/>

长期以来，照亮正确音符进行演奏的音乐键盘一直被吹捧为学习如何演奏的快速而简单的方法。它们看起来也很有趣。[Shootingmaker]已经开发了一个类似的概念，[有一个键盘外观，覆盖着 led(Youtube 视频，嵌入下方)。](https://www.youtube.com/watch?v=D2VWIVyrJ5M)

该项目由一个 PCB 组成，其中面具的设计模仿了一架钢琴的黑白音符。这使得*看起来像一个键盘*，但据我们所知，它实际上并不像一个键盘那样工作。所有的笔记都配有 APA102 可寻址 led，在 Teensy 3.2 板的控制下，以 USB-MIDI 模式运行。Teensy 接收 MIDI 数据，然后根据哪个 MIDI 通道发出音符，指示各个 led 以不同的颜色闪烁。

这是一种有趣的可视化 MIDI 数据的方式，我们认为结合一个基本的合成引擎来制造一些噪音会更有趣。我们怀疑将该项目集成到现有的仪器中也不会太难。对复制项目感兴趣的人可以在 Github 上获得软件。[你也可以用 MIDI 来控制霓虹灯](https://hackaday.com/2018/10/11/midi-controlled-neon/)。

 [https://www.youtube.com/embed/D2VWIVyrJ5M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/D2VWIVyrJ5M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

