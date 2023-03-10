# 私人实验室西贡庆祝迟到的阿杜伊诺日

> 原文：<https://hackaday.com/2019/06/06/fablab-saigon-celebrates-a-belated-arduino-day/>

好了，我们刚刚离开五月，步入六月，为什么我们要谈论 Arduino 日——传统上是 3 月 16 日^日的一个活动，在那里创客们聚集在一起分享项目？我住在胡志明市，活动倾向于在五月中旬举行，但热情和协作精神同样强烈。由令人敬畏的当地创客集团[私人实验室西贡](http://fablabsaigon.org)组织，由 [Intek Institute](http://intek.edu.vn) 提供场地，展示了一些整洁的项目以及一些来自当地公司的演讲。

这个活动给我的第一个印象是，这里的创客运动是如此年轻——大多数参与者还在高中或大学早期。相比之下，当我第一次学习使用汇编语言的 AVR 微控制器时，我才 23 岁(当 Arduino 开始获得牵引力时，船实际上错过了我)。我不禁觉得自己有点过时了，至少在我们开始兴奋地谈论机器人之前(我带了几个)。看起来，对电子产品的痴迷是不分年龄限制的伟大均衡器。

## 特斯拉线圈、闪烁电路和机器人赛跑

在展出的项目中，有一个低功率的特斯拉线圈，可以愉快地产生小火花，打开附近的 CCFL 灯泡，还可以产生一点等离子体。

![](img/764315177fce7c26a75db936da47df00.png)

有一个学习焊接的研讨会，参加者可以随时参加，制作出巧妙的死虫式晶体管多谐振荡器电路。

![](img/35ede52e90a4ce37e9fce5f7dcf9f311.png)

你们中的许多人将会熟悉[非稳态多谐振荡器电路](http://electrosome.com/astable-multivibrator-transistors),这里被看作是对电子学和焊接的一个流行介绍。但如果你不是，这是一个很好的开始，因为你将了解几个不同的组件，结果有闪烁的灯光…同时让你的 Arduino 免费用于其他项目！有人也带来了一些关于使用 GSM 模块的演示。

接下来是一个车间，在那里，漫游者式机器人由当地开发的 STEM 教育套件制造，该套件名为 [GaraStem](http://garastem.com) 。从根本上说，它是一个装满指令的 tacklebox，激光切割的机箱部件，Arduino 兼容板和传感器，以及用于智能手机的 Android 控制应用程序。它看起来简单又有趣，我希望像这样的 STEM 机器人套件在我小时候就有了。我不禁感到有点嫉妒——当我在高中时，我们在我的区域所拥有的只是偶尔的科学展！

![](img/3fdb4309cfe67d29bf94e5aef38dc841.png)

当然，任何时候一个以上的遥控机器人在同一个地方，比赛是必要的，我们就这样做了。完全出于巧合，地板被刷成了看起来像跑道的样子。

## 来自硬件创业公司的演讲

除了项目和研讨会之外，还有一个来自当地公司的关于他们正在做什么的跟踪会谈。其中一家名为 [Indruino](http://www.indruino.com) 的公司设计了自己的 Arduino 电路板，用于工业环境，以及所需的所有功能。他们演示了一个很好的三相电机速度控制器，并谈论了他们为使平台适合工业应用所做的工作。

![](img/b3ed9338f1cd570b8d2dc036c7b9b78d.png)

至少，我可以说他们的电路板充分利用了光隔离器、安全连接器和高质量屏蔽 DC-DC 转换器。根据他们的小册子，他们已经在许多工厂部署了工业触摸屏和冷冻干燥系统控制器——这并不奇怪，因为冷冻干燥食品是过去几年在越南真正起飞的一个行业，在当地设计是一个很好的举措。

当地一家设计模块化假肢的初创公司 Vulcan Augmentics 在那里展示了他们在实用人机界面方面的工作。由于各种各样的原因，在越南有相当多的各种年龄的截肢者，因此任何更好地为他们服务的努力都是值得赞赏的。可惜当时他们的假肢不是在海外就是在用，所以我无法检查硬件。尽管如此，这是一个很好的例子，说明我们作为一种爱好学习的技能有一天可以发展到我们可以对另一个人的生活产生积极影响的地步。

我展示了一些物联网使用案例和演示，其中许多我已经在这里写过了，还有一些关于安全性的重要性和实现的说明，比如带有 AES 或 TLS 的 MQTT。我还谈到了在失去连接的情况下为物联网设备定义可靠故障状态的方法。虽然这是一个极端的例子，但你不能让一个大型机器人撞到墙上，因为在连接断开之前收到的最后一个命令是“前进”！当然，有一种观点认为，我们不应该一开始就轻率地将危险的机器人连接到互联网上，但这并不十分有趣，控制系统方面的教训仍然适用。这很有趣，没有机器人、人类或建筑受到伤害。

![](img/9afc328eda608506dd9faca9c7047c1f.png)

Chúc mừng sinh nhật Arduino!

## 甚至蛋糕也是高科技的

在一天结束时，有必要的蛋糕(草莓酱)。当地的面包店有一种类似杏仁蛋白软糖的东西，他们可以在上面以惊人的高分辨率打印，因此蛋糕上有一些非常好的图像。

该活动以一场小竞赛结束，一些工具包被捐赠作为最高分的奖品。

总的来说，这次活动的社区意识很强，尽管出席人数相当多，但组织得很好。我向西贡私人实验室致敬。