# 在一个振荡器里面

> 原文：<https://hackaday.com/2021/02/21/inside-an-oscillator-with-ken-shirriff/>

我们总是很高兴看到[Ken Shirriff]尝试新的东西，这个月他正在研究石英振荡器模块。现在，你会认为这些没什么大不了的。一块石英板和某种转换器，对吗？但是正如[Ken]提到的，“模块中发生的事情比我预期的要多……”

如果你曾经想去盖设备，像这样的大型混合模块是一个很好的开始，因为你不需要外来的化学物质进入内部。[Ken]在进来的时候设法打碎了易碎的水晶晶片。里面还有一个小的 CMOS 集成电路芯片。该拿出显微镜了。

如果你关注[Ken]的博客，你就会知道他对分析 IC 骰子并不陌生。振荡器 IC 是一个非常标准的 Colpitts 振荡器，但它也提供可编程分频器和输出驱动。

该电路使用一些配置异常的电容器。[Ken]花时间指出 CMOS 逻辑结构。如果你以前没有看过[肯]的深潜，这是一个很好的介绍。

可以了解更多[晶振理论](https://hackaday.com/2018/12/08/crystal-oscillators-explained/)。几年前，我们用一些测试设备来表征一种晶体的[。](https://hackaday.com/2018/06/20/analog-discovery-2-as-a-vector-network-analyzer/)