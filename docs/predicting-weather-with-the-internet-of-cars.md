# 用车联网预测天气

> 原文：<https://hackaday.com/2019/02/18/predicting-weather-with-the-internet-of-cars/>

遵循这个思路:汽车有传感器，汽车在大范围内频繁使用，汽车是天气状况的最终分布式传感器网络。

许多年前，当我又浪费了我生命中的一大块时间坐在我早晨通勤的线性停车场时，我沉思着一定有办法阻止这种疯狂。我想:*如果有一种方法可以让汽车相互告知减速的位置，那会怎么样？*这是在智能手机出现之前很久的事了，所以必须用强硬的方式。我设想每辆车可以有一个小型 GPS 接收器和某种无线收发器，将车辆的当前位置发送到中央服务器，然后中央服务器将每条道路的总速度数据发送回用户的汽车。一个小显示屏会向你显示热点，并允许你选择一条替代路线。天才！我终于找到了我的十亿美元的想法。

可悲的是，这是不可能的。似乎几天后，地球上的每个人口袋里都有了一部装有 GPS 的智能手机，我想象中的复杂系统现在很容易用软件实现。可笑的是，我选择不追求我的想法的原因之一是，我认为没有人会愿意让一家公司访问他们的位置信息。我一点也不知道。

因此，我怀着极大的兴趣阅读了一篇文章，该文章声称来自联网汽车的[挡风玻璃雨刷数据可以用来预防洪水](https://techxplore.com/news/2019-01-vehicles-windshield-wipers.html)。一开始我真的以为这是一个笑话，就像《T2》中的一部巨蟒剧团的小品《T3》。但当我通读这篇文章时，我想到了我很久以前的想法，相当于一个分布式传感器平台，实际上可能不仅仅是用于检测交通堵塞。

## 当下雨的时候

[![](img/696c35deab51c44c8593f7d1f14c4927.png)](https://hackaday.com/wp-content/uploads/2019/02/main_and_university_charlottesville_during_flash_flood_comparison.jpg) 

一点小雨要干什么？上下图相差 15 分钟。pawemm(这个蒙太奇)；Nyttend(原始照片)[ [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0) ，[via Wikimedia Commons](https://commons.wikimedia.org/wiki/File:Main_and_University,_Charlottesville,_during_flash_flood_(comparison).jpg)

马上，我们将规定上面链接的文章标题与实际研究的内容相比有点牵强。这篇文章暗示，OBDC 数据正在被实时捕获和挖掘，以开发一个车队周围环境条件的高分辨率图片。虽然这显然是密歇根大学研究论文[的作者认为他们的结果领先的地方，但离他们现在的位置还很远。](https://www.researchgate.net/publication/330450358_Windshield_wipers_on_connected_vehicles_produce_high-accuracy_rainfall_maps)

这项研究旨在解决土木工程师和城市规划者面临的一个非常具体的问题:很难预测山洪会在何时何地发生。要做到这一点，你需要准确地知道哪里在下雨，下多大的雨，精确到一个非常精细的粒度。相对于大多数城市地区的面积而言，带有雨量计的固定气象站很少，而且不能提供足够的空间分辨率来很好地显示小区域的降雨强度，例如那些经历微暴的区域。天气雷达有利于提供广域覆盖，在一定程度上填补了雨量计之间的空白，但它也存在分辨率问题。这里的想法是将一个仪表化车辆车队的历史挡风玻璃雨刷使用与天气雷达档案和过去风暴的固定雨量计读数相关联，以查看雨刷使用数据是否可以增加传统的降雨量测量。

## 填补空白

也许不出所料，他们发现司机倾向于在下雨时打开雨刷，雨下得越大，雨刷调得越快。但更重要的发现是，通过将挡风玻璃雨刷数据和天气雷达数据置于贝叶斯过滤网络，天气雷达可以更新，以定位实际上正在下雨但雷达错过的区域，并在雷达坚持下雨的降雨模式中找到“漏洞”。

[![](img/74eeed9d76ec5baad45f98067a332c34.png)](https://hackaday.com/wp-content/uploads/2019/02/rain-v-wipers.png)

Wiper data fills in the gaps, finding a calm hole (L) and a local downpour (R) that weather radar missed. Source: [Bartos et al](https://www.researchgate.net/publication/330450358_Windshield_wipers_on_connected_vehicles_produce_high-accuracy_rainfall_maps), [CC BY](https://creativecommons.org/licenses/by/4.0/legalcode).

这些更新绝不是小规模的局部阵雨；雷达错误解释的更新区域大约有 10 公里宽。鉴于一些地方流域的规模，特别是在城市地区，对这一地区“下雨”和“不下雨”的评估可能会在准确预测山洪暴发方面产生影响。

尽管这篇文章有些雄心勃勃，但这项研究只是为联网汽车可以用作远程移动传感平台的未来奠定了基础。人们可以想象，不仅可以获得高分辨率的降雨数据，还可以从外部温度计获得局部温度报告，从防抱死制动和牵引力控制系统数据获得路况评估。

在我们现在所处的位置和城市规划者从行驶在街道上的大量联网车辆中获得高分辨率空间和时间数据的那一天之间，存在着巨大的障碍。但是在有大量数据需要挖掘的地方，你可以确信有人计划利用它。这在多大程度上有利于生成数据的人还有待观察，但目前来说，知道挡风玻璃雨刷可以在某种程度上用于预测山洪爆发是非常酷的。