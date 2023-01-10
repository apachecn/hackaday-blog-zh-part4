# 降压转换器的短路跟踪器

> 原文：<https://hackaday.com/2022/03/10/short-circuit-tracer-for-a-buck/>

几乎你今天找到的每一个电表都有一个连续性测试仪。连接探针，如果有短路，它会发出哔哔声，如果没有，它不会发出哔哔声。但是短在哪里呢？当试图测量一个与许多其他元件相连的元件时，这是另一个问题。[学习电子维修]想要有一个工具来发现电路板上的短路，并想要建立一个测试仪，使用 [4 线电阻测量](https://www.youtube.com/watch?v=P_2GGNr4q1s)来隔离被测设备，而不必对电路进行手术。他的 1 美元建筑出现在下面的视频中。

视频的第一部分讲述了双线和四线电阻测量背后的理论。Let 展示了几个示意图，但他提到，在某一点上，他展示了一个不正确的示意图(12:03)，而不是之前正确的示意图(10:35)，并提到了这一点，但如果您浏览视频，您可能会感到困惑。

引入电容短路的旧显卡是一个很好的演示。仪表能够判断出短路在哪里。这些探针不会赢得选美比赛，但它看起来是可行的。测量实际上是由恒流源引起的电压降，因此读取实际电阻并不方便，但它会告诉你支路在哪里短路。如果你有一个恒定电流的工作台和一些额外的电线，你实际上可以做到这一点，基本上是免费的。

在之前，我们已经讨论过 [4 线测量，重点是如何使引线电阻归零，但同样的想法也适用。如果你更喜欢你在视频](https://hackaday.com/2019/06/05/circuit-vr-resistance-measurement-with-four-wires/)中的[解释，我们最近看到了一个。](https://hackaday.com/2022/01/07/how-many-wires-do-you-need-to-measure-a-resistor/)

 [https://www.youtube.com/embed/P_2GGNr4q1s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/P_2GGNr4q1s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

