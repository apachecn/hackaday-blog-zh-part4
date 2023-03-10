# 给你的推文增加刺痛感的电池

> 原文：<https://hackaday.com/2020/09/27/a-battery-to-add-a-tingling-sensation-to-your-tweets/>

联网情趣用品是在工作中(甚至是在家里)给你的伴侣一个惊喜的好方法，也是给异地恋增添情趣的好方法。对于一些额外的刺激，他们还增加了潜在的将你所有非常敏感的私人数据暴露给公众的刺激——但是，嘿，这不是我们应该感到奇怪的地方。然而，他们的漏洞问题确实很常见，足以使他们成为安全会议的常客，所以还有什么比简单地邀请整个 Twitter 加入你的行列更好的以毒攻毒的方法呢？嗯，[太空巴克]为此建造了合适的设备:[*双 Oh 电池*，一种 AA 电池形式的开源脂肪电池供电的 ESP32 板](https://hackaday.io/project/169304-double-oh-battery)，作为通过 WiFi 控制设备电源电压的替代产品。

[![Battery and PCB visualization](img/ca4ab07c0bab761d48e322de916d4f0f.png)](https://hackaday.com/wp-content/uploads/2020/09/double-oh-assembly.gif)

Double-Oh Battery with all the components involved

在其最简单和最便宜的形式中，振动玩具只不过是一个带有开关的电池供电的马达，即使是具有不同强度水平和模式的更复杂的玩具，通常也仅限于十种左右的品种，最终可能会有所欠缺。为了在不实际拆卸设备的情况下对其进行改进，[Space Buck]最初建造了输出电平 的[*插槽机械手，这是一个直接挤压到电池上的微小电路板，具有预编程的模式来启用和禁用电源电压——或者将其变成闹钟。但可以理解的是，从长远来看，重新编程模式可能会令人讨厌，所以增加 WiFi 和网络服务器似乎是合乎逻辑的下一步。当然，更多的功能需要更多的空间，所以为了保持 AA 电池的外形，双 Oh 电池的 PCB 现在搭载在一个更小的 10440 LiPo 电池上。*](https://github.com/heyspacebuck/SMOL)

但是，如果你不把它开放到互联网上，那么有一个带网络服务器的 WiFi 振动器有什么意义呢——它还可以用来做留言簿？因此，在一些大胆的实验中，[太空雄鹿]展示了这个项目的潜力，将它与他的推特账户挂钩，并让公告推特的赞和转发接管控制权，无疑增加了惊喜的欢迎元素。以 Instagram 为例，这可能也是一个很好的虚荣奖励系统的改进，或者是一个很好的礼物，向你圈子里所有寻求关注的人发出信息。

抛开所有的乐趣不谈，远程控制设备的电源是一个有趣的项目，尽管由于整个电池的性质，它的应用范围可能相当有限，但[常见的 Sonoff 开关](https://hackaday.com/tag/sonoff/)可能看起来有点不适合这里。如果这激发了你对锂电池的兴趣，看看[【勒温·戴】的初学者指南](https://hackaday.com/2020/06/11/a-beginners-guide-to-lithium-rechargeable-batteries/)和[【鲍勃·巴德利】对其化学成分的深入探究](https://hackaday.com/2019/10/07/better-battery-management-through-chemistry/)。