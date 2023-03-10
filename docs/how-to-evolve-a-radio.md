# 如何发展无线电

> 原文：<https://hackaday.com/2018/11/12/how-to-evolve-a-radio/>

进化算法是一个有趣的研究课题。不是依靠人类的聪明才智和调查来创造新的设计，而是给算法一个要实现的目标，并创建“后代”，以进化的方式迭代，以创建每一代都更接近目标的后代。

这种方法可以应用于电子电路的设计，有时被称为“硬件进化”。杜克大学的一个团队正是试图这样做，目的是利用进化技术制造一个振荡器。

该团队使用了一个名为“可进化主板”或 EM 的平台。EM 是一个由附加计算机控制的平台，由可重新配置的固态开关组成，允许附加电路组件以每种可能的组合互连。这些组件实际上可以是任何电子组件；在这个实验中，使用了 10 个双极晶体管。

进化算法被赋予一个奖励输出幅度和频率的适应度函数，旨在创建一个工作在 25KHz 的振荡器。然而，研究小组注意到一些有趣的突现行为。该算法倾向于奖励电路的放大行为，导致许多配置振荡不佳，但放大了环境噪声。最终，该算法开发出了充当收音机的电路配置，从周围环境中拾取并放大信号，而不是自己振荡。进化算法不仅利用了电路元件之间的相互作用，还利用了开关矩阵引入的寄生电容等效应，并且似乎将 PCB 电路走线用作天线。

该团队得出结论，电路设计中使用的进化算法忽略了人类对电路工作方式的先入之见，并将利用有时不可预测和意想不到的效果来实现他们的目标。这是一个祝福也是一个诅咒，让非传统的设计脱颖而出，但也创造了可能无法在通用环境中很好工作的电路。例如，如果您的“振荡器”依赖附近的噪声源工作，它可能会在现场不可预测地工作。

我们以前见过进化算法被使用，[比如被应用于机器人设计](https://hackaday.com/2016/03/14/making-dumb-robots-evolve/) [。](https://hackaday.com/2016/03/14/making-dumb-robots-evolve/)