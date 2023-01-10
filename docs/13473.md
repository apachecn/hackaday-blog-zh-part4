# DIY 基于 Arduino 的电动汽车充电器省钱，看起来专业

> 原文：<https://hackaday.com/2022/04/28/diy-arduino-based-ev-charger-saves-money-looks-pro/>

电动汽车(ev)是一个热门话题，我们报道的大多数关于它们的攻击都集中在从内燃到电动的转换上。这些都很好，我们希望将来能看到更多。还有一个不经常涉及的方面:如何给电动汽车充电——特别是商业化生产的电动汽车，而不是 DIY 的那种。这就是[fotherby]接手的项目:[为他的起亚](https://www.instructables.com/Electric-Vehicle-EV-Charger/)提供 7.2 千瓦的电动汽车充电器。

面对花费 900 英镑(约 1100 美元)购买由合格电工安装的商用设备，[fotherby]决定做一些研究。该项目没有超出他的范围，他给自己一个先发制人的机会，找到了一个商业外壳和电缆，最初只是一个没有内部结构的陈列室。

Arduino Pro Mini 为充电器提供了大脑，源代码和所有需要的信息都在 GitHub 上。然而，该指南的突出之处在于深入探究了这些充电器的工作原理，以及它们是如何简单明了。

处理主电源和安装如此重要的套件意味着 DIYer 存在固有的风险，而[fotherby]通过包括接地故障检测电路令人钦佩地解决了这些问题。结果是，如果有任何类型的接地故障，它将在低于可能伤害人类的阈值的速度和水平下关闭整个电路。[fotherby]通过彻底测试电路并记录结果来支持这一点，表明充电器符合商业标准。尽管如此，这不是电动汽车爱好者的第一次项目，所以我们觉得有必要说“不要在家里尝试这个”，即使这正是展出的内容。

最后，节省了几百英镑，DIY 充电器和商用充电器一样好用。确实是一个伟大的黑客！虽然这些并不常见，但我们确实在大约一年前介绍了另一款开源电动汽车充电器，你可能也想了解一下。

 [https://www.youtube.com/embed/pCcnrtT_gis?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/pCcnrtT_gis?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

