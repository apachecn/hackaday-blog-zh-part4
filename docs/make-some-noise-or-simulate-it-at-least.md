# 至少制造点噪音或者模拟一下

> 原文：<https://hackaday.com/2020/11/03/make-some-noise-or-simulate-it-at-least/>

噪声是生活中的事实，尤其是在电子电路中。但是在我们的纸上原理图和我们的模拟中，没有噪声。如果你在电路板上闪烁 LED，你可能不在乎。但是，如果你正在做一些更具体的工作，优雅地处理电噪声是很重要的，模拟可以帮助你。[Ignacio de Mendizábal]有一篇关于使用 LTSpice 仿真 EMC 滤波器的精彩文章[，可以帮助您入门。](https://www.allaboutcircuits.com/technical-articles/designing-and-simulating-emc-filters-ltspice/)

噪声有多种分类方式，[Ignacio]从共模噪声和差分噪声入手，共模噪声是指电流同向流动的噪声，与电路的正常工作无关，而差分噪声是指电流同向流动的噪声。

本文展示了如何对这两种噪声进行建模，还介绍了如何对真实电路元件进行建模，以便更精确地捕捉真实滤波器的行为。有了一个好的噪声模型和一些波特图，滤波器设计工作将变得更加容易和稳定。

EMC，或称电磁兼容性，对商业设备至关重要。测试是昂贵的，所以你在模拟中做得越多越好。如果你需要开始使用 [LTSpice](https://hackaday.com/2017/10/09/one-mans-tale-of-emc-compliance-testing/) ，我们有你。