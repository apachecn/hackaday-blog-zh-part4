# 隐藏在 USB 端口中的微控制器如何变成隐藏在 USB 端口中的 FPGA

> 原文：<https://hackaday.com/2018/12/25/how-a-microcontroller-hiding-in-a-usb-port-became-an-fpga-hiding-in-the-same/>

当您想到微控制器开发时，您可能会想到带有芯片的试验板或 USB 连接的电路板。但是 Tim Ansell 描绘了一个几乎完全隐藏在 USB 端口内部的 ARM 开发板。[他在 2018 年黑客日超级大会上的讲话](https://youtu.be/ZOMLzuNyWac)讲述了这个故事，以及其他一些内容。休息之后，看看新发布的视频，以及更多的演讲细节。

Tim 是 Tomu 的创造者，这是一个微型的 ARM Cortex M0+板，我们在一月份第一次提到过它。该板的一侧有一个 Silicon Labs EMF32，另一侧有四个与 USB 端口接口的走线，还有两个 led 和两个电容触摸按钮。这种外形来自他在亚马逊上发现的双因素认证设备——他很感兴趣，但对价格犹豫不决。

了解微型通用第二因子(U2F)设备的组件成本非常低。他花了一个周末布置电路板，在处理了他一般的 SMD 技能后，他完成了一些工作原型。问题出现在实际移植一些 U2F 固件到设备上。由于没有时间深入项目的这一部分，他开始尽可能多地分发这些开放硬件板，最终有人为其编写了 U2F 代码(是谢尔盖·格鲁什琴科，[这是回购](https://github.com/gl-sergei/u2f-token))。

## USB 端口中的 FPGA

现在蒂姆开始着手下一件大事。他[将 Tomu 的外形适配到一个名为 Fomu](https://github.com/im-tomu/fomu-hardware) 的 FPGA 板上，目前[正在](https://www.crowdsupply.com/sutajio-kosagi/fomu)开展一场活跃的众筹活动。该主板将附带一个已经加载的 RISC-V 内核，可以使用 DFU(或大容量存储)进行编程。现在这是一个流行的举动，因为很多人都想玩 RISC-V 或 FPGA，这里有一种方法可以做到这两者，而实际上不必随身携带额外的设备。

有些人可能会想:在 FPGA 很难连接外部电路的情况下，你能做些什么？您可以练习为 RISC-V 和其他内核添加外围设备，但也许您应该思考的是:如果我有一些专用的并行处理功能，我可以用我的笔记本电脑做什么？该板携带 Lattice iCE40UP5K、1 MB 闪存、128 kB RAM，运行频率为 48 MHz，与开源 IceStorm 工具链兼容。

蒂姆的超级演讲在下面，他甚至为演讲准备了幻灯片。

 [https://www.youtube.com/embed/ZOMLzuNyWac?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ZOMLzuNyWac?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

