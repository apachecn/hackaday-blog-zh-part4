# 寒冷天气刺激需求，破坏发电机，德州电网陷入困境

> 原文：<https://hackaday.com/2021/02/16/trouble-with-the-texas-power-grid/>

面对异常寒冷的冬天，孤星之州的居民正遭受轮流停电，这有点令人震惊。首先，德克萨斯的冬天？第二，难道不是夏季热浪造成了那个地区的滚动停电？

如果你向一个欧洲人提起德克萨斯州，他们可能会想到牛仔、石油、热门电视节目*达拉斯*，如果他们是欧洲黑客读者，可能会想到半导体巨头德州仪器。美国唯一一个有脱离条款的州也有自己独立于邻近州的电网。

[![An accurate and contemporary portrait of a typical Texan, as understood by Europeans. Carol M. Highsmith, Public domain.](img/54d2f9d76af02ae7f99e88afe2f85297.png)](https://hackaday.com/wp-content/uploads/2021/02/lossy-page1-1280px-thumbnail.tif.jpg)

An accurate and contemporary portrait of a typical Texan, as understood by Europeans. Carol M. Highsmith, [Public domain](https://commons.wikimedia.org/wiki/File:%22Horses_on_the_Beach,%22_a_horseback-riding_operation_on_Padre_Island,_Texas,_is_an_incomplete_description_of_the_experience,_as_this_photograph_attests._Some_guests_get_a_short_excursion_aboard_the_LCCN2014633476.tif).

当然，美国是一个足智多谋的地方，这是不可能的，当我们从远处看着停电地图上激增的红色方块时，我们喊道。事实证明，这一次，我们被告知定义德州的独立倾向可能是它的毁灭。我们已经习惯了我们的欧洲国家被连接到欧洲大陆电网的其余部分，但是因为德克萨斯电网是独立的，它无法在需要的时候从它的邻居那里吸取电力。

让我们深入研究维护电网的机制，目前不幸的德州人是试验对象。

## 煤、天然气、核能和风力发电机的组合被寒冷淘汰

如果一个电网简单得就像一组发电站全时连接到一个恒定的负载上，那么它的运行将是一件相对简单的事情，在一端铲进某种燃料，在另一端接收电力的好处。可悲的是，为人类供电的现实从来都不是那么可预测的，电网公司一直在玩预测可变需求的游戏，以使其与发电量相匹配。整个发电站都有提供近乎瞬时额外电力的特定应用——你可能还记得[我们对英国电山](https://hackaday.com/2017/07/12/places-to-visit-electric-mountain/)的报道。电网策略师把预测我们的行动作为他们的工作，因为这些行动关系到每一分钟的用电量。

由于德克萨斯州夏季酷热，他们已经习惯了用电高峰期，因为德州人会集体打开空调，而这个毗邻墨西哥湾的州冬季相对温和，对系统压力不大。但是在这里，我们有一个完美的能源设施风暴，由于天气原因无法应对额外的需求，德克萨斯州转向电热取暖。

他们目前的寒流已经用冰冻的北极取代了相对温和的气候，导致了冰暴，截至周日早上，冰暴已经停止了该州一半的风力发电。根据电网运营商得克萨斯州电力可靠性委员会(ERCOT)的说法，周日开始的寒冷天气导致[大多数发电厂离线，这些发电厂是天然气、煤炭或核能的组合。(墨西哥也有断电的报道](https://www.houstonpublicmedia.org/articles/news/energy-environment/2021/02/15/391479/rolling-power-blackouts-in-effect-across-texas-as-massive-winter-storm-drives-demand-for-electricity/)[是因为从德克萨斯来的天然气管道](https://www.npr.org/2021/02/16/968230163/millions-without-power-in-texas-northern-mexico-as-blackouts-and-bitter-cold-con)被冻住了。)虽然 2020 年风力发电确实占德州发电量的四分之一，但据报道，这些涡轮机在冬季月份没有满负荷运转。

[![North America, in power grid terms. Fjbfour, Public domain.](img/fa9d236fe9b5d4b154ecf2a00f88bdc3.png)](https://hackaday.com/wp-content/uploads/2021/02/Nercmap.jpg)

North America, in power grid terms. Fjbfour, [Public domain](https://commons.wikimedia.org/wiki/File:Nercmap.JPG).

需要的时候，能不能向邻居借一杯能量？北美大陆有两个大型电网，落基山脉两侧各有一个，还有一些较小的电网，德州互联就是其中之一。其存在的原因是历史的，其延续的部分原因是因为作为一个单一国家的实体，它不受某些联邦或国际(与加拿大)法规的约束。它与邻国有一些相对适度的 DC 互连，但它们的容量不足以让较温暖的州的发电机填补空缺。有一个雄心勃勃的计划是[一个更大的 DC 互联项目，将东部和西部电网与德克萨斯电网](http://www.tresamigasllc.com/index.php)连接起来，这反过来给我们一个机会来看看电网是如何同步的。

## 相位同步使得连接交流电网变得棘手

[![Huge thyristors used in the converter plants of the DC link between North and South Islands, New Zwaland. Marshelec, CC BY-SA 3.0 <https://creativecommons.org/licenses/by-sa/3.0>, via Wikimedia Commons](img/98ef45b748521e81bc76d810eb94f970.png)](https://hackaday.com/wp-content/uploads/2021/02/1024px-Pole_2_Thyristor_Valve.jpg)

Huge thyristors used in the converter plants of the DC link between North and South Islands, New Zealand. Marshelec, [CC BY-SA 3.0](https://commons.wikimedia.org/wiki/File:Pole_2_Thyristor_Valve.jpg).

连接两个交流电网不只是简单地将它们连接在一起，因为[它们的交流频率和相位必须完全匹配](https://hackaday.com/2017/07/05/how-do-they-synchronize-power-stations-with-the-grid/)才能正常工作。德克萨斯州电网与其邻居的标称频率相同，都是 60Hz，但实际上，如果不采取不切实际的措施，关闭整个州的电源并同步重启所有发电机，频率和相位就会有细微的差异。因此，在电网之间传输电力时，解决方案是在中间阶段将其转换为 DC，然后以正确的电网频率和相位转换回交流电。许多海底电缆，如连接英国、斯堪的纳维亚和欧洲大陆的电缆，采用了这种方法，这意味着这些电网是为了交易电力而连接在一起的，但不是同步的。因此，当 2018 年科索沃[的政治僵局导致负荷失衡，使欧洲电网频率陷入螺旋式下降](https://hackaday.com/2018/03/09/europe-loses-six-minutes-due-to-sagging-frequency-and-international-politics/)时，英国电网未受影响。这就是前面提到的雄心勃勃的美国电网互联的工作方式，来自所有三个电网的 DC 链路在新墨西哥通过超导电缆互联实现额外的效率提升。

在大多数黑客读者遇到的电力规模下，在低功率电源电路中到处使用开关调节器甚至一两个断路器来管理是轻而易举的事情。在一个电网、一个国家或一个大洲的规模上，单个半导体开关器件可以有一栋小房子那么大，工程师们不仅要考虑电力处理问题，还要考虑人类行为和地缘政治。如果你是一个德州的黑客读者，正在躲避一场寒流，那么你会得到我们的同情和最美好的祝愿，希望迅速解冻，同时，对于我们其他人来说，值得记住的是[这可能很容易发生在其他任何地方](https://hackaday.com/2019/09/07/anatomy-of-a-power-outage-explaining-the-august-outage-affecting-5-of-britain/)。

标题图像包括美国地图、Wapcaplet、 [CC BY-SA 3.0](https://commons.wikimedia.org/wiki/File:USA_States_Map_-_Educational.svg) 。