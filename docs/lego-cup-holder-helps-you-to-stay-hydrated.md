# 乐高杯架帮助你保持水分

> 原文：<https://hackaday.com/2022/01/04/lego-cup-holder-helps-you-to-stay-hydrated/>

多吃水果，多运动，多喝流质；传统上，一月初是实施新年计划的时候。大多数常见的方法只需要意志力，但是如果你的目标是保持水分，那么就可以得到一些帮助。[Pepijn de Vos]设计了[一个乐高杯架和一个附带的桌面应用程序](http://pepijndevos.nl/2022/01/01/keep-track-of-how-much-you-drink-with-lego.html)，它会准确地告诉你到目前为止你喝了多少水，让你更容易每天喝八杯水。

基本的想法很简单:杯架包含一个称重传感器，可以感知你的饮用容器的重量。如果重量减少，则会向您的电脑发送一条消息，详细说明减少的重量。如果重量增加，则玻璃杯一定被重新装满，之前的重量被忽略。这样，应用程序只需要将所有报告的数量加起来，而不必补偿空杯子的重量。

棘手的是将称重传感器整合到乐高结构中。它需要摆弄一些柔性系统软管，以确保平台的重量只落在称重传感器上，同时仍然足够稳定，可以安全地容纳一整杯水。称重传感器通过放大器和 A/D 转换器读出，而 USB 通信由 Teensy 3 处理。

[Pepijn]修改了一个现有的 GNOME 桌面小工具，以显示一个杯子图标和消耗的总体积，从下面嵌入的视频来看，这似乎工作得非常顺利。所有的代码，甚至一套完整的乐高构建说明都可以在该项目的 Github 页面上找到。如果仅仅监测你的液体摄入量对你来说还不够，那么看看这个设备，如果你喝得不够多，它就会淹没你的桌子。

 [https://www.youtube.com/embed/eixtwrICMIs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/eixtwrICMIs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

