# las atmega 中的时间和精度

> 原文：<https://hackaday.com/2022/01/31/time-and-accuracy-in-las-atmegas/>

在微控制器代码中，您是否需要确保两个任务之间有一个精确的时间间隔？你知道精确和准确的区别吗？今天，[Jim Mack] [告诉我们如何在管理时间时将定时器和中断推到极限](https://escmdxi.wordpress.com/2022/01/05/jagged-precision-borrowed-accuracy/)，同时保持它适用于一直受欢迎的 ATMega328P 目标！不时地，有人决定在给定的平台上推进可能的边界，而今天的规则是在 Arduino 环境的约束下编码。然而，你应该看看[Jim]的帖子，即使你使用 Arduino 作为骂人的话——纯粹是为了所有的理论见解，并附有硬件精确的例子！

这将有助于任何黑客实现，比如说，电机编码器读数，信号频率计算，或建立一个小工具实时处理或修改音频。为了让您了解本文的示例，[Jim]首先向我们介绍了精度和准确度之间的区别，然后向我们展示了一个看似简单的任务——每秒创建 2400 个中断。虽然看起来很简单，但当晶振时钟频率不能完全除以应用所需的采样频率时，问题很快就会出现！这只是所展示的隐藏复杂性的所有例子的一个例子，当你最终在你的黑客追求中遇到这样的例子时，你可以使用它们附带的解决方案。最后，[Jim]给出了其他资源的链接，如果你需要更深入地研究这个主题，你可以研究这些资源。

保持我们的项目符合时间的推移可能是一个问题，我们已经做了很多年了—[校准你的 RC 振荡器](https://hackaday.com/2020/12/30/improve-attiny-timing-accuracy-with-this-clock-calibrator/)是任何 ATTiny 项目的必经之路。如果你曾经决定让一个中断外设来帮助你解决定时问题，我们在过去已经深入讨论过这个话题，通过一个三部分系列来描述[的好处](https://hackaday.com/2015/09/18/embed-with-elliot-interrupts-the-good/)、[的缺点](https://hackaday.com/2015/09/25/embed-with-elliot-interrupts-the-bad/)和[中断的边缘情况](https://hackaday.com/2015/10/02/embed-with-elliot-interrupts-the-ugly/)。寻找更现代的目标？我们关于 STM32 使用中断的文章是尝试现代工具的好方法。