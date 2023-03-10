# 开发一个自动化的 CAN 总线黑客工具

> 原文：<https://hackaday.com/2019/07/22/developing-an-automatic-tool-for-can-bus-hacking/>

在过去，汽车仪表板上的一个物理按钮或开关会被连接到它所控制的任何设备上。这种组合中可能有一个继电器，但仍然不难通过线束跟踪电线，并找出它们的去向。但是今天，这个概念越来越成为一个古怪的记忆。

[![](img/25a995d20297d48727296dead130ceb2.png)](https://hackaday.com/wp-content/uploads/2019/07/canscan_detail.jpg) 假设你的现代汽车甚至有物理按钮，按下其中一个按钮可能会通过 CAN 总线发送一条信息，接收设备(希望)会对此做出响应。[【TJ Bruno】知道与它一起工作是多么令人生畏，他一直在开发一些软件，这些软件有望使 can 总线用户界面的工作更快更容易](https://medium.com/@tbruno25/stop-installing-aftermarket-switches-f4091921f9c2)。最终，他希望他的工具将允许用户快速将定制硬件集成到他们的汽车中，而不必在仪表板上钻孔进行物理控制。

但是如果你是那种不喜欢别人帮你做事的人(可以肯定，因为你正在读 Hackaday)，不要担心。[TJ]首先概述了如何利用 MCP2515 芯片在 Arduino 上读取和解析 can 消息。他一行一行地分解他的样本草图，解释它是如何工作的，这样即使你以前从未接触过 Arduino，你也应该能够得到正在发生的事情的要点。

事实证明，读取 CAN 总线上的消息并对其采取行动相当简单。棘手的部分是弄清楚你在找什么。这就是[TJ]正在编写的代码发挥作用的地方。他的程序不必手动检查通过网络的所有信息并试图确定它们对应的内容，而是在用户重复按下他们想要识别的按钮时进行监听。有了足够的样本，代码可以自动定位到正确的罐 ID。

所有这一切的好处是，您可以用车辆现有的控制装置激活售后功能或硬件。需要举例吗？看看[【TJ】用同样的技术给他的 2017 款雪佛兰科鲁兹加装的前视摄像头](https://hackaday.com/2019/05/09/sniffing-can-to-add-new-features-to-a-modern-car/)。

[https://player.vimeo.com/video/348961986](https://player.vimeo.com/video/348961986)