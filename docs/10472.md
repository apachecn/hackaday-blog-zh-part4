# 无需焊接即可升级 Arduino 纳米内存

> 原文：<https://hackaday.com/2021/06/20/arduino-nano-memory-upgrade-with-no-soldering/>

好吧，我们坦白交代。[设计构建销毁]并没有真正给他的 Arduino Nano 增加任何内存。但与股票设置相比，他确实多获得了大约 1.5K 的程序空间。诀窍？在一些 Nano 板和克隆上，引导装载程序被设置为使用大块保留内存，但是 Optiboot 只需要一小部分保留内存。通过[重新编程引导加载程序并改变配置保险丝](https://www.youtube.com/watch?v=-MynHAz7TsI)，您可以回收未使用的内存。

当然，你不能轻易覆盖串口上的引导程序和保险丝，以防止你的设备阻塞。下面的视频显示了如何连接另一个 Arduino 来进行编程。你也可以使用任何你碰巧有的专用 AVR 程序员。奇怪的是，Uno 已经使用 Optiboot 和相同的处理器，并且设置正确，视频显示了两者在默认状态下的配置差异。

当然，取决于你从哪里得到你的纳米设备和它们的年龄，你可能已经有了这个设置，在这一点上你不会得到任何东西，但你应该能够很容易地告诉你是否需要通过这些步骤。如果 Optiboot 支持的话，同样的技巧可能也适用于你周围的任何旧的 Arduino 板。你能用多余的内存做什么？也许[语音识别](https://hackaday.com/2021/05/26/speech-recognition-on-an-arduino-nano/)？

 [https://www.youtube.com/embed/-MynHAz7TsI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/-MynHAz7TsI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

