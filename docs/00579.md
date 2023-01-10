# 电磁场:TIM，一台中继计算机

> 原文：<https://hackaday.com/2018/09/08/electromagnetic-field-tim-a-relay-computer/>

我们可能都很熟悉计算机的历史，以至于我们知道最早的计算机是非常简单的设备。虽然早期的电子机器如 Colossus 或 ENIAC 是非常复杂的电子管架，但一旦表示为原理图或逻辑门网络，它们对于今天的电子工程师理解它们的操作将是相对简单的。那些对计算历史有深入研究的人可能听说过康拉德·楚泽在 20 世纪中期的工作，他的基于继电器的机器比完全电子化的机器早了好几年。

一台基于继电器的计算机可以简单到由家庭建筑商来建造，在最近的电磁场黑客营[Rory Mangles] [上，他概述了他在学校时建造的 TIM 继电器计算机](https://www.youtube.com/watch?v=RfXrT619jBw)。这是一个引人入胜的故事，从基本原理开始，描述了从简单的二进制加法器到最终的完全图灵计算机的一系列 TIM 设备。他描述了他的 ALU 的设计过程，最终采用 1 位串行设计以节省继电器。

该机器具有哈佛架构，程序路径由纸带组成，代码从纸带直接运行。指令集叫 BLT，当然是 Tim 的 Basic 语言的意思，还有一种 T++汇编语言。通过循环纸带，循环和`if`语句被处理成经典的图灵机。最初的 TIM 已经有几年的历史了，但是他透露他最近把它从存储中取出来，并添加了一个并行端口。因此，演讲的最后部分是一个演示，打印一个“Hello World”。

我们已经把完整的视频放在了休息时间的下面，同时我们足够幸运的是[Rory]带着 TIM 来到 EMF Hackaday 读者村参加我们的“带来一个黑客”活动，所以标题图像是我们有机会检查它时的图像。如果你想知道更多，他有一个网站，上面有更多关于 TIM 的细节。

 [https://www.youtube.com/embed/RfXrT619jBw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/RfXrT619jBw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

