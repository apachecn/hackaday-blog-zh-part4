# 没有疼痛的复阻抗

> 原文：<https://hackaday.com/2019/09/07/complex-impedences-without-the-pain/>

任何一个头发花白的电子工程师都会告诉你，射频工作是*辛苦*的。保持阻抗匹配可能是在较低频率下将电线切割成一定长度的情况，但在厘米和毫米波长的情况下，这就变成了一种黑暗的艺术，由神秘而昂贵的测试设备辅助，凡人无法企及。矢量网络分析仪或 VNA 可能是许多人可望而不可及的，但[托马斯·wątorowski]在这里告诉我们如何通过一些电阻、数学和一点横向思维[，它的功能可以用一个更简单的工作台](https://mightydevices.com/index.php/2019/08/complex-impedance-matching-using-scalar-measurements-math-and-resistors/)来复制。

这种方法不适合胆小的人，因为你可能在大学时学过各种各样的数学，但在课程结束后，你会带着感谢从记忆中溜走。该方法包括测量与天线串联的已知值电阻器的回波损耗，这些数字允许计算天线阻抗的实部和虚部。还有一项工作，这种方法不能确定天线是电容性的还是电感性的。利用电容或电感匹配网络重复测量，可以确定这一点，并计算适当匹配元件的值。

如果你对这类工作感兴趣，[先从 RF 设计入门](https://hackaday.com/2016/03/23/michael-ossmann-makes-you-an-rf-design-hero/)开始。

> [使用标量测量、数学和电阻的复杂阻抗匹配](https://mightydevices.com/index.php/2019/08/complex-impedance-matching-using-scalar-measurements-math-and-resistors/)

[https://mightydevices.com/index.php/2019/08/complex-impedance-matching-using-scalar-measurements-math-and-resistors/embed/#?secret=a4BaY2gN9q](https://mightydevices.com/index.php/2019/08/complex-impedance-matching-using-scalar-measurements-math-and-resistors/embed/#?secret=a4BaY2gN9q)