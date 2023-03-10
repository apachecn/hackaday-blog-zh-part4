# RF Shield 将 Arduino(和 PC)变成短波收音机

> 原文：<https://hackaday.com/2020/02/14/rf-shield-turns-arduino-and-pc-into-shortwave-radio/>

微控制器倾向于消耗其他种类的电子设备。你曾经用 555 完成的一个项目现在可能有一个便宜的微控制器在里面。音乐合成器？遥控控制器？最有可能的是，现在全部基于微控制器。我们一直认为射频电子产品不会受到这种影响，但过去的一二十年证明我们错了。软件定义无线电或 SDR 意味着您可以尽快将 RF 信号转换为数字信号，并在软件中完成所有其他工作。如果你想了解 SDR，Elektor 现在为 Arduino 提供了一个便宜的 RF 屏蔽罩。基于 Si5351 的电路板使用该振荡器 IC 将 RF 信号下移到音频，然后供 PC 进行更多处理。

该板可以单独使用，也可以作为包括书籍在内的套件的一部分。还有一系列关于 Elektor 的文章。下面的视频中还有一段来自 Elektor 的关于主板的回顾视频。

我们偷看了原理图，屏蔽更多的是让 Arduino 通过改变振荡器频率来控制无线电，而不是执行 SDR 功能。IQ 信号通过麦克风或线路输入插孔出现在 PC 的声卡上，并没有真正路由到 Arduino。

这是一个遗憾，因为一些 32 位的 Arduinos 也许可以用正确的硬件做一些有趣的事情。此外，许多有能力的 CPU 和 FPGA 板具有 Arduino shield 兼容布局。这可能会导致一些有趣的可能性。

话说回来，Arduino 上有一个可编程信号源并不是一件坏事，与旧版本的电路板相比，新电路板为振荡器信号提供了更容易的突破。

如果你想了解更多关于 SDR 是如何工作的，试着从[电子表格](https://hackaday.com/2019/11/15/dsp-spreadsheet-iq-diagrams/)开始。然而，如果你想升级到更实际的东西，试试我们在 [GNU 电台](https://hackaday.com/2015/11/12/your-first-gnu-radio-receiver-with-sdrplay/)的系列节目。

 [https://www.youtube.com/embed/jvt_9QmuoVo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/jvt_9QmuoVo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

