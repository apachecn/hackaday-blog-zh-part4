# 了解 DMX512 基础知识

> 原文：<https://hackaday.com/2021/10/15/learn-dmx512-basics/>

如果你做过现代灯光特效，你可能听说过 DMX，也被称为 [DMX512](https://www.youtube.com/watch?v=SsDJyOMiliA) 。有没有想过引擎盖下到底发生了什么？如果是这样，那么你应该看看[EEForEveryone]关于这个话题的视频，你可以在下面看到。

DMX512 的核心使用 RS485，但增加了软件层和功能。该视频使用 OSI 模型来展示系统的工作原理。

当然，RS485 只是像串口一样的物理层。DMX 标准定义了实际的协议。如果您以前没有使用过 RS485，这里有一个关于差分信号的很好的解释，以及为什么它在高数据速率或长信号路径时很重要。还讨论了替代物理层，如网络 DMX512 和无线 DMX。

名称的 512 部分指总线上设备的最大数量。然而，通过网络的变化，你可以使用一根以太网电缆连接多达 400 个 DMX 总线到一个网络设备。那可是相当多的 DMX 频道。每个通道是一个字节，因此，例如，典型的 RGB LED 消耗三个通道。

我们见过背包里的 DMX。如果你做得对，DMX 不仅可以对音乐做出反应，它还可以成为创造音乐的乐器的[的一部分。](https://hackaday.com/2018/11/23/led-ifying-a-guitar-part-two/)

 [https://www.youtube.com/embed/SsDJyOMiliA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/SsDJyOMiliA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

