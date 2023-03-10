# 一个定制的 FPV 显示器让球迷开心

> 原文：<https://hackaday.com/2018/09/05/a-custom-built-fpv-monitor-to-keep-the-fans-happy/>

如果你要乘坐具有 FPV 功能的飞机，无论是四轴飞行器还是固定翼飞机，如果旁观者想戴上你的谷歌眼镜，你不应该感到惊讶。当然，我们希望你有足够好的飞行视线，不需要*戴着*谷歌眼镜就能保持在空中，但这确实让你更难完成观众想看的那种技巧和动作。所以如果你想上演一出好戏，观众真的需要自己的展示。

[![](img/82be55d72324e3126bb88d6abcc6ffb6.png)](https://hackaday.com/wp-content/uploads/2018/09/diyfpv_detail.jpg) 不幸的是，就像狂热的 FPV 飞人【迈克尔·德莱尼】发现的那样，即使是“便宜”的机票也要花掉你至少 100 美元。所以他做了任何有自尊的黑客都会做的事情，他开始建立自己的。[利用一系列现成的组件，他能够建造一个非常令人印象深刻的显示器](https://hackaday.io/project/160893-diy-homemade-fpv-monitor)，让观众通过他的四轴飞行器的眼睛观看，其成本不到市售产品的一半。虽然即使他没有设法击败一个交钥匙显示器的成本，我们认为它会比这个高度定制的设备更值得。

监视器的核心是 Boscam RX5808 5.8 GHz 接收器，由 Arduino Pro Mini 控制。接收器的视频输出被发送到用于 Raspberry Pi 的 4.2 英寸 TFT 屏幕，在激光切割木制外壳的背面有一个 128 x 64 I2C 有机发光二极管，用于显示当前选择的频道和诊断信息。

这个项目的一个特别好的地方是用于将所有元件连接在一起的定制 PCB。[Michael]本可以走一条简单的路线，将设计发送出去进行制作，但却采用了用酸蚀刻他自己的电路板的传统方法。虽然他确实通过使用激光和预敏化覆铜板使过程现代化了一点，但随着激光雕刻器成为黑客武器库中更常见的组件，这种方法似乎越来越受欢迎。

我们之前已经介绍过[使用 RX5808 和 Arduino 组合创建频谱分析仪](https://hackaday.com/2016/01/26/using-arduino-for-quadcopter-spectrum-analyzers/)，以防你想做的不仅仅是观察你的朋友做 powerloops。