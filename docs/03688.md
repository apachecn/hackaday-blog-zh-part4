# CPAP 监视器提醒佩戴者出现故障

> 原文：<https://hackaday.com/2019/08/01/cpap-monitor-alerts-wearer-to-malfunctions/>

持续气道正压通气机是睡眠呼吸暂停和其他呼吸问题的常用治疗工具。使用它们的一个常见问题是面罩在睡眠期间移位，因此不能给患者提供气道压力。[【孙斌】决定尝试解决这个问题](https://hackaday.io/project/166715-digital-manometercpap-machine-monitor)。

该项目包括一个安装了 MPXV7002DP 压力传感器的 Arduino。该传感器用于监控 CPAP 管道中的压力。如果压力有规律地变化，很可能系统正在工作。然而，如果压力保持在大致恒定的水平，这表明面罩不再适合佩戴者，或者存在另一个问题。在这种情况下，该设备会发出蜂鸣声来唤醒佩戴者，提醒他们检查设备。

这是一个简单的解决问题的方法，让我们惊讶的是，大多数 CPAP 机器在出厂时并没有内置这种功能。在修改任何医疗设备之前小心谨慎是很重要的，尽管我们看到许多黑客冒险在这一领域进行创新。

The [HackadayPrize2019](https://prize.supplyframe.com) is Sponsored by: [![Supplyframe](img/79a7db035b8a2b6c2b7b0895c45b7de8.png)](https://supplyframe.com/)  [![Digi-Key](img/ba094a14c430ab81591a2abdc54a5363.png)](https://hackaday.io/digikey)  [![Microchip](img/5023ef0b7ff1aee311cba9b54a3ac9fe.png)](https://hackaday.io/microchip)