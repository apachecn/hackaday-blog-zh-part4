# 廉价 PSoC 使电化学研究成为可能

> 原文：<https://hackaday.com/2018/08/04/cheap-psoc-enables-electrochemistry-research/>

你可能认为电化学听起来像一个深奥的领域，穿着实验室外衣的科学家在复杂的仪器前辛勤工作，发表只有其他电化学家才会喜欢的论文。你可能是对的，但只是部分对的，因为电化学几乎涉及现代生活中的一切。为了证明这一点，只要看看你最近的口袋就知道了，假设那是你放智能手机和为它供电的电化学电池的地方。

电化学是对化学反应的电学性质的研究，确实需要复杂的仪器。然而，这并不意味着这些仪器必须打破拨款预算，正如[Kyle Lopin]用[展示的这个由一个芯片和一个电容器组成的极其简单的恒电位仪](https://hackaday.io/project/160071-easy-to-build-psoc-based-potentiostat)。恒电位仪控制电化学电池中电极上的电压。这种电池有三个电极——工作电极、参比电极和反电极。在这些电极之间以及通过所研究的溶液的电子流揭示了关于反应的还原和氧化状态的重要性质。[Kyle]没有将他的电池连接到昂贵的恒电位仪，而是使用 Cypress 可编程片上系统开发板来完成所有工作。只需将 PSoC 插入 USB 端口进行编程，将电极连接到 GPIO 引脚，并可选地添加一个 100 nF 电容来提高片上 DAC 的精度。下面的视频涵盖了整个过程，尽管画外音几乎听不见。

还不确定电化学？看看这个 2018 年 Hackaday 奖的参赛作品，它利用[生命的电化学让手机起死回生](https://hackaday.com/2018/07/27/micro-organisms-give-up-the-volts-in-this-biological-battery/)。

 [https://www.youtube.com/embed/OCPO-TYS1mw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/OCPO-TYS1mw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

