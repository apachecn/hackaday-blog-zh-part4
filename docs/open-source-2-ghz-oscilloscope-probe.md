# 开源 2 GHz 示波器探头

> 原文：<https://hackaday.com/2020/05/07/open-source-2-ghz-oscilloscope-probe/>

如果你从事高速信号方面的工作，你会很快意识到探测本身就是一门艺术。仅仅有一个快速示波器是不够的；你必须有足够快的探测器来处理你想要看到的信号。在这个领域，任何旧探针都不行:你在低带宽示波器上经常看到的经典 RC 探针的输入电容开始严重加载远低于 1 GHz 的电路。这就是为什么我们真的很高兴看到[Andrew Zonenberg 的]新的[2 GHz 电阻探针开源设计在 Kickstarter](https://www.kickstarter.com/projects/azonenberg/akl-pt1-2-ghz-passive-oscilloscope-probe)上获得成功。

这种新型探测器的设计看起来似乎很简单。该电路被称为 Z [0] 探针、传输线探针或电阻探针，作为一个分压器工作，由高速示波器输入的 50 欧姆输入阻抗和一个外部电阻组成，以减少被测电路的负载。在这种情况下，输入电阻选择为 500 欧姆，产生 10x 探头。理论上，制造这样一个探针就像在一根同轴电缆的末端焊接一个电阻一样简单。你可以做到这一点，但在实践中，优化设计要复杂得多。从原理图中可以看出，在这些频率下，仅选择正确阻值的电阻并不能将其截止。即使是微小的 0402 尺寸电阻也有影响响应的寄生电容和电感，选择增加正确电阻但降低整体容性负载的器件组合会产生巨大影响。

[![](img/f3ee145bcef73b01c312e81d999510e7.png)](https://hackaday.com/wp-content/uploads/2020/05/2GHz-probe-schematic_had.png)

2 GHz Passive Probe Schematic

不要被愚弄:相对简单的原理图掩盖了这种设计的复杂性。在这些速度下，PCB 布局就像电阻本身一样是一个组件，要使传输线，尤其是 SMA 尺寸发射正确并不容易。通过结合使用 Sonnet EM 仿真器建模和经验测试，[Andrew]最终得到了一个在 1.98 GHz 范围内平坦(+/- 1 dB)的设计，10-90%上升时间为 161 ps。那是一个快速探测器。

探针有几种选择，从完全装配的可追踪规格到自己动手焊接的版本。你可能知道你需要这些选项中的哪一个。

我们真的很喜欢看到这种知识和彻底性融入到一个项目中，我们也很乐意看到 Kickstarter 项目达到它的目标，但也许最好的部分是这个设计得到了许可的开源许可。在这种情况下，开发板布局是关键；原理图可能只告诉你电路中实际发生的一半情况，而自己搞定 PCB 可能是一项漫长而令人沮丧的工作。所以，看看这个项目，如果你还没有适合你最快的望远镜的探测器，造一个，或者更好的是，[支持这个令人兴奋的设计](https://www.kickstarter.com/projects/azonenberg/akl-pt1-2-ghz-passive-oscilloscope-probe)的发展。

我们以前见过[安德鲁的]示波器工作，像 [*glscopeclient，*他的远程示波器实用程序](https://hackaday.com/2019/05/30/glscopeclient-a-permissively-licensed-remote-oscilloscope-utility/)。