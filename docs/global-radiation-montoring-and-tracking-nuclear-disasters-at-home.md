# 全球辐射监测和跟踪国内核灾难

> 原文：<https://hackaday.com/2019/08/28/global-radiation-montoring-and-tracking-nuclear-disasters-at-home/>

我们中的许多人并没有过多考虑我们所在地区的辐射水平，直到一场核灾难袭来，问题被提出。辐射监测是一项重要的工作，无论是从公共卫生的角度来看，还是作为监测武器开发等事情的一种方式。那么为什么要这么做，怎么做，关心的公民在关注事情上能起到什么作用？

## 谁在看？

![](img/3aa7a65c76483078f72b36db3caf8543.png)

IRSN helped develop crucial atmospheric dispersion models for use in nuclear accidents. Pictured is the spread of the radioactive plume after the Chernobyl disaster in 1986.

作为环境保护的一部分，大多数国家都建立了一系列政府运营的监测站来监测大气辐射。日复一日，这些数据可能并不特别有趣——报告的背景辐射波动很小或没有波动。但是这些监测站在紧急事件中被证明是非常宝贵的，它们提供了检查放射性物质通过大气扩散的手段。这些组织收集的大气数据通常在危机发生时与土壤和水样本一起使用，以帮助当局确定安全区域，保护民众免受过度辐射。

![](img/012f564bb26d78e24e5c066c9e4888ae.png)

Many monitoring networks also plot the location of nuclear power plants and other relevant sites on their maps.

法国组织 I*Institut De radio protection Et De séreténucléaire*在过去的核事故中一直很活跃，帮助跟踪和模拟放射性物质的扩散。他们的测量结果被用于开发[切尔诺贝利羽流](https://www.irsn.fr/EN/publications/thematic-safety/chernobyl/Pages/overview.aspx)的模型，他们还对[福岛灾难](https://www.irsn.fr/EN/publications/thematic-safety/fukushima/Pages/overview.aspx)进行了重大研究。更广泛的欧洲监测由 EURDEP 承担，在撰写本报告时，其网站经常无法访问。

美国有自己的辐射监测网络。它通过环境保护署在 RadNet 的旗帜下运作。

其中一些小组允许通过网络界面对收集的数据进行近乎实时的监控。其他较小的参与者包括 RadiationNetwork.com 和 T2 的核应急跟踪中心。

## 天崩地裂和禁核试组织

![](img/7e8b309a9d255ec57af3b70042100ab6.png)

Modelling showing the expected spread of radiation in the atmosphere following the Skyfall incident, courtesy of CTBTO.

世界舞台上的另一个主要角色是全面禁止核试验条约组织，简称 CTBTO。他们负责一个由 300 多个站点组成的庞大的全球网络，监测辐射水平，并部署一套广泛的其他传感器，旨在帮助跟踪全球核试验的证据。该组织最近制造了新闻，在最近的[天降导弹测试故障后，俄罗斯运营的监测站离线](https://hackaday.com/2019/08/20/echos-of-the-cold-war-nuclear-powered-missiles-have-been-tried-before/)。与其他团体不同，禁核试组织不公开允许访问从他们的站点收集的数据。然而，他们偶尔会发表公众感兴趣的材料。在天崩地裂事件中，他们公布了[这个显示辐射云](https://twitter.com/SinaZerbo/status/1163179404136210433)预期流动的模型，以及[来自最初爆炸的地震和次声数据。](https://twitter.com/ctbto_alerts/status/1160130156922642433)

## 谁在监视守望者？

国家行为者可能经常试图掩盖他们的错误，随着政府监控站神秘地离线，勇敢的黑客可能希望获得此类数据的独立来源。有几个这样的项目，从拥有和操作自己的监测硬件的公民科学家那里收集数据。虽然这些电视台摆脱了政府所有权的束缚，但它们也有自己的一系列问题。由个人爱好操作，不能保证正常运行时间。许多工作站在数据收集方面有很大的差距，因为所有者没有拔掉设备的电源，或者将 Raspberry Pi 用于另一个项目。此外，没有办法验证数据的质量。读数必须与该区域的平均基线进行比较。如果一个站被移动，即使只是从住宅内移到住宅外，也会影响基线读数，从而在数据中产生混淆的尖峰和变化。也很难阻止专门的恶意行为者攻击此类设备。

![](img/f28f55ba888d8d9fc079e24032648b18.png)

uRADMonitor PCB shown on top of its metal case

尽管如此，任何希望为这样一个监测网络做贡献的人都可以很容易地开始。只需一个树莓派和一个简单的盖革计数器套件，就可以创建一个与一些更基本的政府电台没有太大区别的电台。虽然这些工具无法监测空气中的精确同位素和详细分析核事件，但它们可以清楚地测量该地区的背景辐射水平，并确定高于平均值的峰值。

最著名的监测网络之一是 [uRADMonitor](https://www.uradmonitor.com/) ，它是 2015 年[黑客日奖的参赛者。](https://hackaday.com/2015/12/07/globally-distributed-sensor-net-monitors-air-quality-and-radiation/)该网络收集来自世界各地的数据，其中大部分站点集中在欧洲和北美。空间站由个人运营，配备了各种硬件——有时还配备了额外的传感器，用于监测空气质量和其他环境因素。[甚至可以从单个站点](https://www.uradmonitor.com/tools/dashboard-04/?open=820000D1)绘制数据图表，选择单个日期范围进行探索。其中一些工具有缺陷，但对坚持不懈的人来说是可行的。

Radmon 是另一个用于记录此类数据的站点。与 uRADMonitor 不同，Radmon 只专注于辐射监测。虽然它的网站是一个更基本的建设，它的特点更符合科学设置。各个站点的图表以清晰易读的格式绘制，原始 CSV 数据可以从去年开始下载。

## 数据冒险:测试运行社区来源的数据

![](img/7b42c49eec76b2c4854ada833f075ad8.png)

This station is sadly typical of many on the open-source monitoring networks. Few conclusions can be drawn from such data.

作为确定这些工具的可能性的练习，我继续寻找，看是否能找到天降导弹事件中辐射峰值的证据。不同监测网络使用的许多不同的网络界面，以及不能准确显示过去日期范围内数据的错误网站，让这一点非常沮丧。

![](img/662b98a73b722224d3fe0f3580d639b9.png)

August 12st spike recorded by a monitor in Sweden

经过许多努力，结果是微弱的。许多站点在收集的数据上有很大的差距，或者各种各样分散的和不太可能的读数。不变的精确读数在许多天内保持不变，这是探测器或网络设置故障的证据，因为放射性衰变是宇宙中更随机的力量之一。其他监测站在不同点的背景水平有很大的变化，这表明测量设备可能被移到了窗台下或房子里。这种转变使得梳理出任何真实数据变得困难。

我们想看到的是，在 8 月 8 日之后的几天里，探测站出现了一系列峰值，这与辐射云穿越欧洲的时间相吻合。根据上面 CTBTO 的建模，我们发现很少可能并不奇怪——预期的云预计主要在俄罗斯上空循环，那里很少有(如果有的话)与公众共享数据的监测站。

![](img/bb0360ac29b43e067e0c1fdaf53c28c9.png)

Recording spike and remain elevated at a monitor in Denmark

我们只在拉德蒙的探测站 *[纳特里克斯](https://radmon.org/radmon.php?function=showuserpage&user=Natrix)* 和 [*oz1ewr*](https://radmon.org/radmon.php?function=showuserpage&user=oz1ewr) 发现了两个尖峰信号。 *Natrix* 是一个位于瑞典的探测站，8 月 12 日有一个清晰的尖峰。这一峰值显然是异常值，是 3 个多月来的最高纪录。在位于丹麦的 *oz1ewr，*站，检测到的辐射量上升更为显著，但与其说是峰值，不如说是上升到新的平均值。然而，在西欧的其他监测器，包括 Radmon、uRADMonitor 或 EURDEP，都没有显示任何我们能找到的显著峰值。

![](img/837da6aa52309819e58418b9c6511709.png)

Data from other sources failed to corroborate any major spike in the days following the Skyfall incident.

不幸的是，在缺乏更多观测站的确证数据的情况下，很难断定我发现的是天崩事件辐射云的直接证据。更有可能的是，欧洲数百个台站中有两个单独经历了完全不相关的本地事件。这项研究向我们展示了辐射监测的价值，无论是在个人层面。这也是一个很好的例子，说明为什么将这些传感器联网是有用的。尽管如此，这也表明在任何环境监测中都非常需要严谨和小心，以免收集的数据在噪音中变得模糊和无用。

## 结论

虽然我们可能还没有找到我们要找的东西，但我希望这些开源监控网络能够继续扩散和改进。在一个新的充满活力的核时代，它们可能只是一个重要的工具。如果您正在考虑运行自己的监控站，请仔细考虑如何实现和维护它，以便生成尽可能多的有用数据。如果你是政府或开源项目的 web 开发人员，考虑如何最好地让那些试图找出数字平均值的人获得数据。而且，如果你是核工程方面的，试着确保你第一次就做对了，因为第二次机会很少。祝你好运！