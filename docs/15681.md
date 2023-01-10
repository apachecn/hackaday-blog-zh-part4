# 晶体管？记忆？等等，都是！

> 原文：<https://hackaday.com/2022/12/18/a-transistor-memory-wait-its-both/>

如果把石墨烯、六方氮化硼、二硒化钨交叉，会得到什么？根据湖南大学研究人员的说法，你可以得到一个场效应晶体管，它既可以作为开关元件，也可以作为存储单元。部分浮栅场效应晶体管或 PFGFET 使用 2D 范德瓦尔斯异质结构来处理隔离的原子层。不幸的是，《自然》杂志上的论文在付费墙后面，但是你可以在[TechExplore]上[阅读摘要](https://techxplore.com/news/2022-12-reconfigurable-device-based-2d-van.html)。

石墨烯充当栅极，晶体管可以在 n 型行为和 p 型行为之间切换。它也可以被配置为开关元件或类似于 EEPROM 单元的存储元件。

具有可配置晶体管类型的一个优点是单个晶体管结构可以产生 CMOS 或互补电路。传统上，CMOS IC 有两种不同的晶体管结构，通常生产其中一种需要额外的努力。

通过施加控制电压脉冲来进行配置。负控制电压产生 p 型 FET，正电压将同一晶体管配置为 n 型。如果你看不到这篇论文，网上的数字[可以让你更好地了解这款设备的设计。](https://www.researchgate.net/figure/Device-configuration-of-the-PFGFET-a-Schematic-of-the-PFGFET-structure-equipped-with_fig1_365477803)

如果你想了解更多关于普通[MOSFET](https://hackaday.com/2016/12/13/ask-hackaday-dude-wheres-my-mosfet/)的知识，我们经常会谈到它们。你也可以从[Bil Herd]获得 CMOS 上的[skinny](https://hackaday.com/2015/08/03/how-cmos-works/)。