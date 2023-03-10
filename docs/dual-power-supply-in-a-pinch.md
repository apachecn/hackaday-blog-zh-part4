# 紧急情况下的双电源

> 原文：<https://hackaday.com/2022/07/02/dual-power-supply-in-a-pinch/>

最近，我需要一个双电压电源来测试一个新来的 PCB，但我通常使用的实验室电源暂时在客户的现场。我有一个 FNIRSI 可编程电源，这将是完美的，但可惜，我只有一个。在我的垃圾箱里翻找的时候，我发现了几个 USB-C 电源传输“触发器”板，这是我为一个即将到来的项目买的。对于手头的任务来说，这些似乎太小了，但是经过一点研究，我意识到它们会工作得很好。

[![](img/84819c85215cd4ffe848e4481d5dc1c4.png)](https://hackaday.com/2022/07/02/dual-power-supply-in-a-pinch/lab-power-supply-front/)

Lab Bench Power Supply

[![](img/9b84d9810502527804fcdbb09a045c4d.png)](https://hackaday.com/2022/07/02/dual-power-supply-in-a-pinch/pd-zoom/)

Substitute Using USB-C PD Triggers

我使用的是许多这类电路板中常用的 USB-C 供电芯片。我的已经预先配置了特定的输出电压，但它们很容易重新跳线到我需要的电压，+5 VDC 和+20 VDC。最具挑战性的方面是实际使用它们——它们只有指甲大小。这个版本在 0.1”中心有通孔输出焊盘，所以我决定将它们焊接到标准 MTA 引脚接头的底部。几个卷曲之后，我就可以启动并运行了，同时还有必要的一对 USB-C 电缆和电源适配器。

只需几美元，这些触发板在你的工具箱里就很有用，既可以用于个别项目，也可以在紧急情况下使用。几年前我们[回顾了这些模块](https://hackaday.com/2020/10/23/a-plethora-of-power-delivery-potential/)，并查看了我们去年报道的更加灵活的[PD Micro](https://hackaday.com/2021/01/16/usb-c-programmable-power-supply-for-any-project/)。