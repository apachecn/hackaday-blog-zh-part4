# 5G 如何可能将天气预报置于风险之中

> 原文：<https://hackaday.com/2019/04/16/5g-buildout-likely-to-put-weather-forecasting-at-risk/>

如果伟大的塞缪尔·克莱门斯今天还活着，他可能会把这句经常被认为是他说的著名的气象妙语改为:“每个人都抱怨天气预报，但我无论如何也不明白为什么！”在他那个时代，天气预报和其他事情一样都是猜测，阅读云和风来预测未来几个小时内可能发生的事情，而且正确的时候也是错误的。几十年来，电报和更好的仪器使预测更加科学，准确性稳步提高，以至于我们现在可以享受 10 天的预测，至少对规划目的是好的，三天的展望在 90%的时间里是正确的。

使这种准确性的提高成为可能的是运行复杂天气建模软件的超级计算机。但是模型的好坏取决于它们用作输入的原始数据，而且越来越多的数据来自高层。一组带有极其灵敏的传感器的卫星监视着地球，几乎实时地探测风和水蒸气的变化。但是，如果负责运行这些系统的人是可信的，那么这些数据的质量面临着一个不太可能的敌人的致命威胁:5G 蜂窝网络的推出。

## 水在哪里？

为了理解新一代无线技术如何对天气预报产生有害影响，看看究竟是什么驱动了天气，以及这些卫星在观察什么，会有所帮助。我们的天气很大程度上是气团差异的结果。压力、温度和湿度，每一个都由来自太阳的能量输入决定，所有这些以一种复杂的方式组合在一起，决定了云将在何时何地形成，风将从哪个方向吹来。遥感这些差异是准确预测天气的关键。

观测天气的卫星主要是被动传感器平台，测量它们下方物体反射或发射的能量。他们收集温度和湿度的数据——压力仍然主要通过地面测量和无线电探空仪来测量——通过用不同的波长观察行星。温度主要是用可见光和红外线的光波长来测量的，但是水蒸气有点难以测量。这就是微波发挥作用的地方，也是天气预测与 5G 部署相冲突的地方。

[![](img/3dbb7eeeb51ff96f98feaf3b1709768b.png)](https://hackaday.com/wp-content/uploads/2019/04/AMSU-A1_instrument.jpg)

NASA’s Advanced Microwave Sounding Unit (ASMU-A1). Source: [ESA](https://www.esa.int/Our_Activities/Observing_the_Earth/Meteorological_missions/MetOp/About_AMSU-A1)

地球上的一切——植物、土壤、地表水，特别是大气中的气体——都吸收微波辐射，并在较小程度上释放微波辐射。测量这些来自太空的信号是携带微波辐射计的卫星的任务，微波辐射计是调谐到微波频率的敏感无线电接收器。通过观察不同波长接收到的信号，并添加有关信号偏振的信息，微波辐射测量可以告诉我们大气垂直柱内发生了什么。

对于水蒸气，23.8 GHz 被证明是非常有用的，但非常有可能受到 5G 的干扰，5G 将使用非常接近的频率。由于微波辐射计是无源接收器，它们可以看到在该范围内发射微波信号的几乎所有东西，比如支持完整 5G 部署所需的数千个蜂窝基站。在 5G 噪音的海洋中丢失微弱但可靠的水汽信号是气象预报员面临的基本问题，这是他们以前遇到过的问题。

## 现实世界的后果

在美国气象学会 2019 年年会上，美国宇航局喷气推进实验室的研究工程师 Sidharth Misra 提交了数据，显示商业企业如何对科学界产生意想不到的后果。在 2004 年到 2007 年间，基于卫星的微波辐射计探测到横跨美国顶部的奇怪弧线上的噪音增加。另一颗卫星也探测到了类似的信号，另外还有从每个海岸和五大湖的水域返回的巨大信号。这些信号原来是地球同步直播电视卫星的反射，从地表反弹回来，淹没了气象卫星试图测量的水汽信号。

[![](img/231cea4c6f55e68ecfbd8c06c39a7c7d.png)](https://hackaday.com/wp-content/uploads/2019/04/interference.png)

Reflections from DTV satellites can effectively blind microwave radiometers. Source: [AMS meeting panel discussion, “The Wizard Behind the Curtain?—The Important, Diverse, and Often Hidden Role of Spectrum Allocation for Current and Future Environmental Satellites and Water, Weather, and Climate”](https://ams.confex.com/ams/2019Annual/videogateway.cgi/id/51518?recordingid=51518)

但是科学家们肯定反应过度了，对吗？像天气预报这样复杂的难题丢失一个数据真的会有那么大的影响吗？大概是的。据估计，由一些气象卫星上的[高级微波探测装置](https://www.esa.int/Our_Activities/Observing_the_Earth/Meteorological_missions/MetOp/About_AMSU-A1) (AMSU)等微波辐射计返回的水汽数据可以将天气预报的误差减少 17%，这是迄今为止几十种其他模式中最大的贡献者。

微波水汽数据的丢失可能会带来灾难性的现实后果。2012 年 10 月下旬，当飓风桑迪席卷美国东海岸时，预报显示风暴将转向西北，在新泽西州登陆。如果微波辐射仪数据不可用，对天气预报的分析显示，风暴以一个宽弧形持续，并在缅因湾登陆。风暴登陆前五天获得的 ASMU 数据为民政当局赢得了准备所需的时间，并可能减少了“世纪风暴”造成的人员伤亡，这仍然是 2012 年最致命的风暴。

[![](img/e76fe4e0dd6b65178fdd81b6401549aa.png)](https://hackaday.com/wp-content/uploads/2019/04/sandy.png)

Superstorm Sandy would have been predicted to track into the Gulf of Maine (red) without microwave water vapor data. It actually landed in New Jersey, as predicted five days out with the satellite data (black).

## 拍卖时间

那么，我们在这个过程中到底处于什么位置呢？上微波灵活使用服务(UMFUS)的许可证的 [FCC 拍卖](https://auctiondata.fcc.gov/public/projects/auction102)于 2019 年 3 月 14 日开始，尽管美国宇航局局长 Jim Bridenstine 和商务部长 Wilbur Ross 要求推迟拍卖。联邦通信委员会主席 Ajit Pai 拒绝了这一请求，称“这一反对缺乏任何技术基础。”

5G 部署会对天气预报产生负面影响吗？不清楚。被许可方需要限制带外发射，但由于需要如此多的 5G 站点来覆盖预期的服务区域，并且关键的 23.8 GHz 水蒸气频率如此接近 UMFUS 频段，因此没有太多的误差空间。一旦 5G 猫从袋子里出来，就很难保护微波频谱的关键部分。

无论发生什么，天气预报都不乐观。UMFUS 拍卖进展迅速，目前已经筹集了近 20 亿美元。愿意在频谱上花这么多钱的公司肯定会不惜一切代价实现他们的投资，最终，不仅科学可能会受到影响，而且生命可能会因为 5G 而受到威胁，因为我们预测危险天气的工具集面临这一新的数据收集挑战。