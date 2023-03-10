# 一个简单的线性电源，做得不错

> 原文：<https://hackaday.com/2022/04/05/a-simple-linear-power-supply-done-well/>

在 2022 年，当寻求电源设计时，寻求开关设计是很正常的。它们重量轻，效率很高，并且通常以合理的价格出售。它们的好处是，令人惊讶的是，很少看到传统的线性电源具有市电频率变压器和整流电路，因此[ElectroBoy]的用于音频放大器的[双电压 PSU 板](https://hackaday.io/project/184651-high-power-rectifier-and-filter-for-amplifiers)值得再看一眼。

这种线性电源的电路非常简单，由变压器、桥式整流器和电容组成。变压器隔离并降低交流电压，整流器将其转换为粗略的 DC，电容器过滤 DC 以尽可能消除交流纹波。在音频电源中，电容器具有双重作用:在播放的音乐产生需求峰值的情况下，为电源提供滤波和脉冲储备。仔细选择是至关重要的，在这种情况下，选择环形电源变压器和优质电容器。

像这样的线性电源和高质量音频的开关设计之间的选择绝不是明确的，可能是我们将在[我们的 Know Audio 系列](https://hackaday.com/2021/06/02/know-audio-start-at-the-very-beginning/)中考虑的事情。理想的属性是低噪声和我们提到的脉冲水库，它可能是公平的说，虽然这两种类型的电源可以满足它们。由于环形变压器的额外费用，线性电源不太可能是两者中较便宜的，但我们怀疑天平倾向于它，因为良好的线性电源更容易设计。