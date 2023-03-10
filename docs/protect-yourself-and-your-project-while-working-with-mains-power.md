# 使用市电时保护您自己和您的项目

> 原文：<https://hackaday.com/2019/06/05/protect-yourself-and-your-project-while-working-with-mains-power/>

当调试普通的低压电路时，你是相当安全的:除非你有一些非常耗电的设备，需要大量的电流，否则不会有太多真正糟糕的事情发生，所以你可以在电气安全规则上有很多自由。对于市电供电的设备，您就没有这种奢侈，知识的缺乏、草率的工作实践或简单的错误都会让您和您的项目付出高昂的代价。虽然你仍然需要知道自己在做什么，并保持必要的谨慎，[Yann Guidon]的最新项目——以及 2019 年 Hackaday 奖的参赛作品——一个电源保护盒,可能会防止简单的错误变成灾难。

使用主电源时，您可以采取一些预防措施。我们都使用过简单的直插式电源板，所以你可以快速切断电流，但[Yann]包括了许多可以以不同方式配置的设备，以安全地试验市电供电的设备。该项目内置于一个坚固的带提手的开顶木箱中，在外观和功能上令人想起传统的试验板。包括许多不同的器件，如果需要，可以重新配置成不同的拓扑结构。

[Yann]包括一个隔离变压器，它不仅可以在意外接地的情况下保护免受冲击，还可以抑制噪声。还有一个自耦变压器，它允许在很宽的范围内调整输出电压进行测试。当然，断路器是必须的，电流表和电压表可以让你随时了解情况。需要时，易于操作的大开关可快速切断电源。

(可能)最后一点是可调输出电流限制，这仍是一项正在进行中的工作。它围绕电流监控继电器和 DPDT 继电器构建，连接成一个闩锁，如果输出电流超过额定电流(相当于 10 W 至 100 W)，它可以断开输出。这是新项目初始测试的最佳选择。

因此，如果你想从事电力项目，仔细看看[Yann]组装了什么，并在开始之前学习适当的安全程序。可以从我们自己的关于电源安全的 Jenny List 的一个伟大系列开始:[第一部分](https://hackaday.com/2016/05/11/looking-mains-voltage-in-the-eye-and-surviving-part-1/)和[第二部分](https://hackaday.com/2016/05/16/looking-mains-voltage-in-the-eye-and-surviving-part-2/)。在外面注意安全！

The [HackadayPrize2019](https://prize.supplyframe.com) is Sponsored by: [![Supplyframe](img/79a7db035b8a2b6c2b7b0895c45b7de8.png)](https://supplyframe.com/)  [![Digi-Key](img/ba094a14c430ab81591a2abdc54a5363.png)](https://hackaday.io/digikey)  [![Microchip](img/5023ef0b7ff1aee311cba9b54a3ac9fe.png)](https://hackaday.io/microchip)