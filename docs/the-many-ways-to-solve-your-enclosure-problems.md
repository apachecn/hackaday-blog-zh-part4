# 解决围栏问题的多种方法

> 原文：<https://hackaday.com/2021/09/15/the-many-ways-to-solve-your-enclosure-problems/>

这里的大部分项目都涉及到某种电子产品，以及某种用来装电子产品的盒子。几乎所有市售的电子产品也是如此。

尽管如此，选择一个外壳还远远不是一个解决的问题。对于简单的电子产品来说，完全有可能花比电路本身更多的时间来获得正确的结果。但大多数时候，我们需要避免陷入硬件的确切位置。

你的住房有大量的选择，虽然许多人默认使用 3D 打印机，但通常会有更好的选择。在这个问题上，我已经犹豫了无数次，我想分享我看到的选择，并帮助你决定哪一个适合你。再来说说圈地！

## 纸板:非常适合外壳和 PCB 布局打样

对于概念验证或短期项目，您需要一些快速、肮脏且临时的东西。为什么不用你手头的一些硬纸板呢？

 [![A cardboard box makes a perfect rough draft of an enclosure.](img/b8aae0aae028e8b004641109656d0191.png "cardboard_enclosure")](https://hackaday.com/2021/09/15/the-many-ways-to-solve-your-enclosure-problems/cardboard_enclosure/) LCD, switch, power supply, microcontroller, and battery are all nestled inside a cardboard box in this proof of concept. [![cardboard pcb with components soldered on to copper tape](img/024ee16b4770e2d6542d74f7380392b2.png "cardboard_pcb")](https://hackaday.com/2021/09/15/the-many-ways-to-solve-your-enclosure-problems/cardboard_pcb/) The top of the cardboard has a printout of the PCB layout, with copper tape in some key areas and SMT components soldered in place. This rough model is used to verify physical dimensions and mechanical functionality within minutes. [![injection molded button in 3d printed enclosure with cardstock pcb and real components](img/ad20322a871b5552544b5daffaf3636b.png "cardboard_pcb_enclosure")](https://hackaday.com/2021/09/15/the-many-ways-to-solve-your-enclosure-problems/cardboard_pcb_enclosure/) The injection molded button used for a different product inside a 3D printed part for testing a new product in development.

硬纸板很容易使用，你可以快速地把接口和连接器放入孔和槽中。借鉴它，塑造它，不惜一切代价。使用卡片纸(如麦片盒)进行更高质量、更精细的加工。在快速原型制作的世界里，cardboard 是生成快速迭代来测试可用性和粗略想法的绝佳选择。它还具有与 0.062 英寸 PCB 相似的厚度，可以快速轻松地打印您的设计，将其粘贴到纸板上，将其剪下，并在您等待真正的邮件到达时有一个临时替代品来完成您的机械工作。

## 塑料食品容器

![Using a yogurt container as the enclosure.](img/f43cf83f42ae687b0e15f1aa3e2bc98a.png)

Mobile disco-turtle robot

当你需要更坚固或防水时，可重复使用的塑料食品包装，包括酸奶容器和 Tic Tac 包装，也可以发挥很大作用。这个击掌移动迪斯科海龟机器人是在一个 5 岁孩子的指导下制作的。酸奶容器装有电池、扬声器、Arduino 和所有电线，保护敏感部件刚好够这个寿命有限的怪物使用。

找到你需要的大致尺寸和形状的东西，根据需要进行修整和钻孔。实用刀片是制作高保真外壳所需的唯一工具，仔细加热或使用胶水可以将零件密封并粘在一起。除非你的目标是一个媚俗的产品，否则你不应该期望做超过一对夫妇，他们的耐用性是有限的，所以预计这将只比纸板持续时间长一点点，更适合潮湿的环境。

## 粘土/可塑塑料

![instamorph enclosure](img/838fbe9ef65e1565d2e83e273ba4a0f6.png)

Using InstaMorph to make a quick plastic electronics case ([Image from InstaMorph](https://www.instamorph.com/ideas/electronics/lcd-display-enclosure))

如果你有模制的技能，并且能把一块材料做成你想要的形状，那么粘土可能是一个不错的选择，或者烤箱烘烤的聚合物(Sculpey)。InstaMorph 是另一种由塑料组成的工具，它在低热下软化并变得可塑。它有片状和颗粒状，可以用热水或空气软化，用手操作直到冷却。

## 使用现有机柜

![takachi enclosures samples](img/b5335984f3786367f33af0bed7635c4e.png)

Takachi Enclosures is just one of many companies with project boxes in a variety of sizes and types. Perfect for small volume high quality projects.

这个选项没有得到足够的重视。现有外壳非常适合小批量生产，弥补了原型和大批量生产之间的差距。 [Polycase](https://www.polycase.com/) 、 [New Age Enclosures](https://www.newageenclosures.com/) 、 [Takachi](https://www.takachi-enclosure.com/) 、 [Bud](https://www.budind.com/) 和 [Hammond](https://www.hammfg.com/) 都是我过去使用过的注塑、挤压或其他预制外壳，可以很容易地进行修改，以满足您的确切需求(不，我们没有被要求提及它们中的任何一个)。

一旦你熟悉了他们的产品线，你就会开始在其他产品中认出他们的外壳。您挑选了一个尺寸和类型合适的外壳，大多数都会提供某种形式的 CAD(或者至少是具有相关尺寸的 PDF 设计图),通常甚至会提供建议的 PCB 轮廓。点一个或几个，你只需要几块钱就能得到你需要的一切。当需要将它投入生产时，你甚至可以给这些公司提供任何所需的铣削图，或者在任何表面上印刷，他们也会为你完成这些工作，只需支付少量的安装费和每个零件的成本。

## 3D 打印

这里不缺少关于 3D 打印的文章，即使有更快、更便宜、看起来更干净的选择，这似乎也是人们的默认选择。

如果你的需求超出了盒子，你必须有某种特殊的外壳来适应特定的形状，或者你试图快速或微型地制作它，那么 3D 打印可能会起作用。你必须拿出你选择的 CAD 程序，或者找到一个现有的设计，这是使这个选项对许多人来说不太容易实现的事情之一，并且可能非常耗时。从好的方面来说，有各种各样的材料可供使用，有 3D 打印并邮寄给你的服务，许多公共图书馆甚至将 3D 打印机作为一项服务提供给你。

## 激光切割

[![A laser cut enclosure for a custom keyboard](img/36b48f79a44494ea9cd8b1db15b39c1e.png)](https://hackaday.com/wp-content/uploads/2021/09/boxes-py-console-by-Wolfpuppie.jpg)

Example of box design form Boxes.py (image source: [Wolfpuppie](https://github.com/florianfesti/boxes/issues/140#issuecomment-656909886))

如果你有机会，激光切割也是一个不错的选择。一般来说，这些都是丙烯酸或胶合板外壳，虽然纸板也很好，边缘要么互锁，要么直。像 [MakerCase](https://en.makercase.com/) 和 [Boxes.py](https://www.festi.info/boxes.py/) 这样简单的可定制的盒子有在线生成器，你可以在下载后修改它们来添加你的孔和切口。

## 注模

注塑模具是大规模生产的行业标准，能够以惊人的速度生产塑料零件并连续运行。它们可以被设计成精确的规格，并且可以使用从几千到几百万个零件。不利的一面是前期成本，基本模具的成本可能高达数千美元，而带有滑块、多型腔和冷却线的高容量硬化钢的成本可能高达数百万美元。[我们已经详细介绍了注射成型](https://hackaday.com/blog/?s=injection+mold)，但是关于注射成型要记住的首要一点是，它不是一次性的，一旦工具被切断，你将无法轻易改变你的设计。

## 其他:数控、铸造和复合材料

还有无数其他的选择。你可以用 CNC 在商店里用木头或金属制作你的外壳。有各种各样的铸造技术，包括 3D 打印模具和在模具内铸造，或者 3D 打印正片，创建硅胶模具，然后在模具内铸造零件。你可以把所有东西都放在一个临时的围栏里，然后把它封起来(实际上是把环氧树脂倒进去填满它)。您可以使用多种方法组合来制作外壳的不同部分，甚至是子组件。我已经 3D 打印和激光切割了支架，用于现有的外壳。

## 结论

在你直接跳到你的 CAD 软件花几个小时设计一个盒子并 3D 打印它之前，考虑一下其他可能更快或更便宜或更好看的选择。当然，这篇文章并不是一个详尽的列表，但是如果我错过了一些重要的东西，请在下面提到它。