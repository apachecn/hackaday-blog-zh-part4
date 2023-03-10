# 无需繁琐模拟的电路阻抗计算

> 原文：<https://hackaday.com/2021/03/02/circuit-impedance-calculations-without-cumbersome-simulations/>

使用 SPICE 等电路仿真软件可以成为模拟现实世界中电路行为的强大工具。另一方面，并不总是需要 SPICE 的所有特性都可用，而且这些程序往往也相当昂贵。为此，【Wes Hileman】注意到了一个机会，可以使用 python 使用[特定、快速的方法来执行阻抗计算，而无需庞大、昂贵的软件，并开发了一个程序，他称之为 fastZ。](https://github.com/whileman133/fastZ)

该软件适用于任何无源元件(电阻、电容和电感)网络，用户可以使用特殊运算符指定并联和串联连接。该程序不仅可以计算组合阻抗，还可以在特定频率下进行频率分析，或者绘制宽频率范围内的频率响应图。它还运行在 python 中，这使得它像导入任何其他 python 包一样简单，并且与构建模拟和期望最好的结果相比，也易于在任何其他 python 程序中实现。

如果您发现自己经常绘制波特图或试图拼凑一个电路仿真来处理您的 python 代码，这种解决方案是一种省去许多麻烦的好方法。让 SPICE 这样的软件与其他 python 程序一起工作是有可能的，[通常会有一些非常有趣的结果](https://hackaday.com/2019/11/30/circuit-simulation-in-python/)。