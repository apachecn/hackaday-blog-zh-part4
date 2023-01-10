# 教授基础知识的一大套逻辑门

> 原文：<https://hackaday.com/2021/01/24/a-big-set-of-logic-gates-for-teaching-the-basics/>

向学生讲授逻辑门通常分为两部分，一部分在白板上讲授理论，另一部分在实验板上进行实践。[shurik179]对白板上易于理解的符号和现实中充满许多门的小型 IC 封装之间的抽象不感兴趣。相反，他建造了一套现实世界的逻辑门，可以连接在一起作为教学工具。

每个“门”由一个大约名片大小的 PCB 和一个丝网组成，PCB 上有 led 显示其输入和输出状态，丝网显示有问题的门的名称和符号。还有一个主 PCB，具有三个种子值 A、B 和 C，用于馈入系统。学生可以将这些值设置为 1 或 0，并将它们馈入到用 3 导体伺服电缆连接在一起的门中，并观察内置 led 上的输入。

这是在课堂上演示逻辑门的好方法。该设计还允许翻转 PCB 以显示负责实现逻辑的实际电子元件，作为更好地理解真实电子设计的桥梁。当然，这并不是唯一的学习方式——[如今，即使是《辐射 4》也有了成熟的逻辑工具包！](https://hackaday.com/2016/06/22/fallout-4-gets-logic-gates-is-functionally-complete/)