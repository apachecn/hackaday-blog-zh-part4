# 无线电变得荒谬

> 原文：<https://hackaday.com/2018/12/21/radio-gets-ridiculous/>

在今年的 Supercon 上有很多精彩的演讲，但是我们真的很喜欢 Dominic Spill 演讲的标题:[荒谬的收音机](https://www.youtube.com/watch?v=THyM4YiWE0k)。让我们面对现实吧，按照你应该做的方式制造收音机、电脑或无人机是一回事。用你不应该用的东西做一个完全是另一回事。这就是多米尼克的方法。在短短的 30 分钟内，他向你展示了两个接收器和两个发射器。是什么让他们可笑？考虑其中一个接收者。它是软件定义无线电(SDR)。一个 SDR 应该有多少位？一点怎么样？可笑？那你就明白了。

Dominic 非常擅长使用普通的微控制器，弯曲它来做奇怪的射频事情，结果非常有趣。例如，试验板 SDR 是一个微控制器，由三部分组成:天线、二极管和电阻。就是这样。如果你错过了 Supercon 的演讲，你可以在下面看到新发布的视频，以及多米尼克演讲的更多亮点。

## 是不是单片机滥用？

![](img/bfc3a80d47a22c75884bc46a36c46eae.png)

RF frontend salvaged from a VCR connected to a microcontroler

当然，他利用了微控制器中的模拟转换以及在软件中产生信号的能力。你可能会认为这将是一个贫血的接收器。当然，这不会是一个高保真远程接收器，但它确实与 GNU 电台接口！

微控制器产生信号的能力意味着你也可以制造发射器。其中一个正在使用的板是一个 GreatFET，实际上是为 USB 设备原型制作的。然而，通过使用 USB 时钟发生器，你可以得到一个灵活的信号发生平台。

这些并不总是非常实用，但也不仅仅是实验室的好奇心。例如，一个演示者在他的汽车上使用了射频进入系统，所以这种技术在野外并不是行不通的。另一个做测向。肯定会有吸引你兴趣的东西，而且有大量的链接可以更深入地挖掘你感兴趣的东西。

我们喜欢把东西变成收音机的项目，比如查尔斯·洛尔(Charles Lohr)把一台 [ESP8266 变成了一台电视发射机](https://hackaday.com/2016/01/31/tv-transmitter-uses-esp8266/)。我们甚至看到了一些 [FPGA 发射器](https://hackaday.com/2018/09/30/icestick-makes-terrible-radio-transmitter/#more-326368)。但是我们最近的兴趣是当 Ted Yapo [把 USB 转串行适配器变成了一个功能发射器](https://hackaday.com/2018/12/06/your-usb-serial-adapter-just-became-a-sdr/)。

**更新:【Dominic 演讲[的幻灯片现已发布](https://hackaday.com/wp-content/uploads/2018/12/Ridiculous-Radios-Supercon-2018.pdf) (PDF)。**

 [https://www.youtube.com/embed/THyM4YiWE0k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/THyM4YiWE0k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

