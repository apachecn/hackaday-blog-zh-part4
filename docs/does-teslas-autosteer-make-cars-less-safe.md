# 特斯拉的 Autosteer 会让汽车变得不那么安全吗？

> 原文：<https://hackaday.com/2019/03/04/does-teslas-autosteer-make-cars-less-safe/>

2016 年，一辆特斯拉 Model S T 型车全速撞上一辆拖拉机拖车，车上唯一的一名乘客当场死亡。当时它正以 Autosteer 模式运行，在撞车前，司机和汽车的自动制动系统都没有做出反应。美国国家公路交通安全管理局(NHTSA)调查了该事件，要求特斯拉提供与 Autosteer 安全相关的数据，最终[得出结论，该车辆的设计](https://static.nhtsa.gov/odi/inv/2016/INCLA-PE16007-7876.pdf)不存在安全相关的缺陷(PDF 报告)。

[![](img/774c9308f26fcff7cc3cc56e617307f4.png)](https://hackaday.com/wp-content/uploads/2019/02/nhtsa_tesla_graph.png) 但《NHTSA 报告》更进了一步。基于特斯拉向他们提供的数据，他们指出，自从在特斯拉令人困惑的“自动驾驶”功能套件中添加 Autosteer 后，严重到需要部署安全气囊的撞车率下降了 40%。这是一个了不起的结果。

因为它太壮观了，一家有调查汽车安全历史的私人公司想看看这些数据。NHTSA 拒绝了，因为特斯拉声称这些数据是商业秘密，所以质量控制系统(QCS) [提起了信息自由法诉讼，以获得报告所基于的数据](https://www.carcomplaints.com/news/2017/lawsuit-nhtsa-freedom-of-information-act-request.shtml)。将近两年后，QCS 最终获胜。

调查数据后， [QCS 得出结论，在增加自动转向系统后，撞车事故可能实际上*增加了*多达 60%](http://quality-control.us/nhtsa_autopilot_safety_claims.html) ，或者可能根本没有。无论如何，NHTSA 提供的数据是不充分的，有奇怪的遗漏，NHTSA 已经收回了他们的安全声明。这个 NHTSA 180 是怎么发生的？我们能从报告中学到什么吗？这与特斯拉宣称的高于平均水平的安全线有什么关系？我们将深入研究下面的数字。

但如果不说别的，特斯拉命运的戏剧性逆转应该凸显出自动驾驶和其他先进汽车技术的安全数据透明的必要性，[这是我们多年来一直呼吁的事情](https://hackaday.com/2016/12/05/self-driving-cars-are-not-yet-safe/)。

## 每百万英里有多少起车祸？

NHTSA 怎么可能得出 Autosteer 减少了 40%车祸的结论，而实际上它却增加了 60%的车祸发生率？这种可疑的“向上”语言是怎么回事？QCS 报告的简短版本可以这样读:特斯拉向 NHTSA 提供了零碎、不完整的数据，NHTSA 对缺失的数据做出了一些对特斯拉极其有利的假设，而这些假设不太可能反映现实。

[![](img/65e355e4f97a8d176bf763a550ea26e3.png)](https://hackaday.com/wp-content/uploads/2019/02/tesla_autopilot.png) 至关重要的是，没有一个关于使用 Autosteer 行驶里程的数据曾经离开过特斯拉。特斯拉给 NHTSA 的，他们声称代表商业秘密的，是安装 Autosteer 前后里程表上的里程数，最后一次检查汽车的里程数，以及是否有安全气囊部署。由此，你最多可以得出安装了 Autosteer 的汽车每英里的事故率，而不是 Autosteer 激活时每英里的事故率。只有特斯拉知道开着 Autosteer 开了多少英里，他们不告诉，甚至政府也不告诉。

## 如何获得+40%到-60%的范围

那么 NHTSA 有没有得到安装了 Autosteer 的汽车行驶了多少英里的数据呢？不完全是。特斯拉给了他们“安装 Autosteer 之前报告的里程数”——里程表值。他们还给出“Autosteer 安装后的下一个里程报告”——另一个里程表值，但不能保证这将与之前的读数匹配，数据在这里变化很大。

对于这两个数字匹配的数据样本，您可以假设这是安装 Autosteer 时的里程数。我们将这些汽车称为“已知里程数”——它们对应于 QCS 报告中的图 1。已知里程数的汽车占样本汽车的 13%，在安装 Autosteer 后，这些汽车的事故率*增加了*60%。在安装 Autosteer 之前，有 32 次安全气囊部署，行驶了 4200 万英里，之后有 64 次部署，行驶了 5200 万英里。乍一看，安装了 Autosteer 的 Tesla 似乎比没有安装的 Tesla 更容易崩溃。(记住，我们不知道 Autosteer 实际使用时的行驶里程。)

数据中另外 34%的车辆在里程表里程数为零时安装了 Autosteer，所以我们将这些称为“工厂 Autosteer”汽车。它们对应于 QCS 的图 2。这些汽车的碰撞率与第一个样本中 Autosteer 之前的时期相似，减少了 Autosteer 的负面安全影响。如果你将这两个样本结合在一起，看起来装有 Autosteer 的汽车比没有安装 Autosteer 的汽车发生碰撞的频率高 37%——几乎是 NHTSA 原始结果的镜像，但比事故增加 60%要好。

[![](img/b4b5e50f77a67b8a90763f30d4d58f03.png)](https://hackaday.com/wp-content/uploads/2019/02/mileage_gap.jpg) 剩余 53%的样本由汽车转向前里程和汽车转向后里程不一致的汽车组成。例如，也许我们知道汽车在里程表上 20，000 英里处没有安装 Autosteer，但它在 60，000 英里处安装了 Autosteer，留下了 40，000 英里的黑暗中间区域。这辆车可以在 20，001 英里的标记处安装 Autosteer，或者在 59，999 英里的标记处安装 Autosteer。

当把安全气囊事故加起来除以里程数时，你用哪一个？NHTSA 假设 20，000 英里——这是“安装 Autosteer 之前报告的里程数”。如何对待这些不完整的数据，以及是否使用这些数据，将决定 NHTSA 汽车方向盘+40%的安全系数和-37%到-60%的安全系数。呸。

## 没有通过气味测试

作为一名前政府统计学家，我的第一直觉是，这些数据有猫腻。为什么 Autosteer 在售后加装的汽车群体中似乎有如此巨大的效果，但在工厂加装时显然没有效果？我不知道如何解释这些差异，但我会谨慎地称之为 Autosteer 安装效果。也许这些早期采用者开车不太谨慎？也许他们更肆无忌惮地使用 Autosteer，因为他们想测试一个新功能？也许早期版本的 Autosteer 有问题？对于缺失的数据，得出的结论怎么会对我们必须做出的假设如此敏感，在+40%和-40%之间摇摆？

[![](img/e0300c4b24c46471da7504cd40be3079.png)](https://hackaday.com/wp-content/uploads/2019/02/redactions.pdf.jpg) 平心而论，NHTSA 最初要求特斯拉提供[难以置信的详细信息](https://static.nhtsa.gov/odi/inv/2016/INIM-PE16007-64338.pdf) (PDF)，这将使他们的工作更具决定性。特斯拉回答说里程表读数是商业秘密，NHTSA 让法官裁定它们不是。

尽管如此，最终特斯拉还是用这个“曝光里程差距”给了他们数据。特斯拉显然也通知了 NHTSA [为什么它不能给他们所要求的数据](https://static.nhtsa.gov/odi/inv/2016/INLE-PE16007-66301.pdf) (PDF)，但是这个原因在 FOIA 的报告中被编辑了。我们只知道 NHTSA 接受了他们的借口。

特斯拉很可能知道里程表的准确读数。毕竟，特斯拉对他们收集的使用中汽车的详细数据感到自豪。当他们自己的 Autosteer 软件被安装时，他们怎么能不知道超过一半的汽车的里程表里程，比 20，000 英里内更准确？请随意在评论中胡乱猜测，因为我们可能永远也不会知道答案。

就数据分析而言，底线是这样的:对于具有可靠数字的数据，安装 Autosteer 似乎与每百万英里撞车次数增加 35%到 60%之间有关。剩下的一半样本有不精确的数据，它是否有利于 Autosteer 取决于基于不良数据的假设。

## 冷冰冰的硬数字，而不是公关宣传

当 NHTSA 发布报告称 Autosteer 导致事故大幅减少时，特斯拉自然欣喜若狂，马斯克也发了推文。现在结果已经发生了变化，他拒绝发表评论。就在 QSC 论文发布之前，特斯拉开始发布[季度安全报告](https://www.tesla.com/VehicleSafetyReport)，但是它们[缺乏有用的数据](https://www.theverge.com/2018/10/4/17937504/tesla-autopilot-safety-consumer-report)。NHTSA 更新了其系统性能评估的说明是一个模糊的小星号脚注:“注意:自从我们发布第三季度报告以来，NHTSA 发布了新的数据，我们在第四季度报告中引用了这些数据。”没错。

特斯拉的安全报告非常简短，缺少数据，而且含糊不清。特别是，特斯拉只报告了使用 Autopilot 驾驶的英里数，auto pilot 是特斯拉驾驶员辅助功能的总称，包括自动紧急制动、自适应巡航控制和车道保持或自动转向。其他汽车制造商非常清楚地表明[自动紧急制动系统有助于减少碰撞](https://www.consumerreports.org/car-safety/automatic-emergency-braking-guide/)，但特斯拉没有为我们分解数字，所以很难说出 Autosteer 特别对车辆安全有什么影响。

最后，特斯拉的报告包括撞车和“类似撞车的事件”，不管这是什么意思。尽管如此，如果你假设特斯拉报告的事件比其他情况下多，那么与美国全国平均水平相比，他们的汽车似乎有很高的碰撞统计数据，即使没有自动驾驶仪。为什么会这样？与其他豪华车相比，特斯拉的优势明显缩小，因为这些豪华车同样没有新手和经验不足的司机。特斯拉的报告还显示，使用自动驾驶比不使用自动驾驶每英里发生的事故更少，但由于你只能在清晰的条件下在高速公路上使用自动驾驶，这也不足为奇。

就潜在特性的安全性而言，很难说这些数字*意味着什么。他们对 NHTSA 的回避行为，加上他们自愿报告的奇怪指标很难激发信心。*

总之，特斯拉提供给 NHTSA 的数据达不到要求，其中 50%的数据因为某种原因被篡改了——这不是我们所认为的透明。我们也不能对他们的自愿安全报告有更多的期望——没有公司会发布可能对他们的业务运营产生负面影响的信息，除非他们被迫这样做。因此，也许我们不应该痛斥特斯拉，而是应该要求我们的政府[认真对待公路安全的透明度](https://www.latimes.com/business/autos/la-fi-hy-tesla-nhtsa-20190214-story.html)，并尽可能支持他们的努力。毕竟，我们都是共享道路上的共同试验品。