# 模拟方式的图形均衡器

> 原文：<https://hackaday.com/2018/10/06/a-graphic-equaliser-the-analogue-way/>

曾经有一段时间，任何高保真音响的前面板上都有一小排滑块，这是一种图形均衡器。在高保真音响中，这些可变增益陷波滤波器阵列只不过是音调控制的花哨版本，但在专业音频和 PA 系统中，它们与更多频段一起使用，以精确均衡场地并消除任何不想要的谐振。

在现代高保真系统中，这项任务是通过软件来完成的，但是[ Grant Giesbrecht ]更希望在那些花哨的音调控制方案中有一个模拟均衡器，而不是专业设备。[他的项目](https://hackaday.io/project/161227-graphic-equalizer-geq-1)是对模拟滤波器设计的一次精彩尝试，也是对均衡器如何组合多个滤波器的一次理解。出乎意料的是，它们的输出没有混合，因为事实证明很难确保所有滤波器都具有相同的增益，相反，它们与通过所有滤波器的信号路径串联。

由此产生的均衡器巧妙地建立在 PCB 上，配有 4 节 AA 电池电源，是一个独立的音频组件。出乎意料的是，这样的模拟均衡器在 Hackaday 已经很少了，所以看到它特别令人高兴。我们更习惯于现成设备的图形显示。