# 你的示波器有多大？一英寸？

> 原文：<https://hackaday.com/2018/09/11/how-big-is-your-oscilloscope-one-inch/>

我们渴望看到【马克·奥莫】进入我们一平方英寸项目的成品。这是一个 [20 兆采样每秒示波器](https://hackaday.io/project/160802-1-square-inch-20msps-oscilloscope),符合外形规格，包括一个微小的有机发光二极管屏幕。我们承认，我们开始考虑是否可以用这些来代替面板仪表，或者为它的存在找到一些其他的借口。不过，我们最终意识到，这可能不太实用，但不可否认它很酷。

有一些 PCB 布局模型，但设计似乎是可行的。PIC32MZ 提供马力。[Mark]计划在芯片的转换器中使用交错模式，以获得每秒 20 兆样本和 10 MHz 的带宽。看起来他会用 DMA 来驱动有机发光二极管。除了有机发光二极管和 PIC，还有一个终端网络和一个可变增益级，仅此而已。

小小的电路板不支持标准 BNC，因此输入是 SMA。我们以前在其他小望远镜上见过。从 PCB 模型来看，看起来边缘也会有一些按钮，所以预计在小屏幕上有一个用户界面。

这是我们举办的第二届[方寸竞赛](https://hackaday.com/2018/08/07/the-square-inch-project-rides-again/)，如果你想参赛，[截止日期已经被延长](https://hackaday.com/2018/09/06/one-square-inch-expanded-in-the-time-dimension/)，但不会太久了。桌上有真钱，包括给获胜者的 500 美元。[测试装备](https://hackaday.com/2018/09/08/see-binary-on-your-breadboard/)似乎是一个受欢迎的主题，虽然如果[上次是任何预测器](https://hackaday.com/2016/01/13/the-best-projects-that-fit-in-a-square-inch/)，还有很多其他的选择。

* * *