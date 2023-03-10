# USB-C 台式电源

> 原文：<https://hackaday.com/2019/11/04/a-usb-c-bench-power-supply/>

台式电源是每个黑客都需要的东西之一，顾名思义，它打算在你的工作台上占据一个荣耀的位置。但是随着他的 DPH5005 工作台电源增加了 USB-C 支持，【Dennis Schneider】随时准备在需要时带着他上路。

[![](img/c01d839404457f7af590c78b46efbda1.png)](https://hackaday.com/wp-content/uploads/2019/10/benchusbc_detail.jpg) 构建从一个普通的 DPH5005 台式电源套件开始，[Dennis]说他对它相当满意，除了他在博客上的帖子中详述的几个问题。即使你不打算用世界上最新最好的通用串行总线技术来修改你自己的套件，如果你已经考虑自己挑选一个，阅读他对电源套件的想法也是很有趣的。

正常情况下，您应该通过电源后面板上的端子为 DPH5005 DC 供电，然后通过前面板上的控制装置对电源进行调节和调整。为了增加对 USB-C 的支持，所有[Dennis]需要做的就是在外壳的背面安装一个 USB-PD 触发模块，配置为协商 20 VDC，并将其连接到 DC 输入。为了将它固定在适当的位置，同时将其与金属外壳隔离，他使用了一块仔细切割的废弃 PCB，并用 Kapton 胶带包裹。

这实际上不是我们看到的第一个便携式台式电源。去年，我们看到一款[从 Makita 便携式工具电池](https://hackaday.com/2018/05/18/hybrid-bench-power-supply-can-also-hit-the-road/)获得输入电源，但我们认为综合考虑，USB-C 选项可能更方便一些。