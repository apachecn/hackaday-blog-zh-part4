# 监测水流和保护大自然面临的挑战

> 原文：<https://hackaday.com/2020/06/30/the-challenges-of-monitoring-water-streams-and-surviving-mother-nature/>

小水道以饮用水和灌溉水的形式给予生命，但当洪水发生时也可能是非常具有破坏性的。在美国，对这些水道的监测主要由美国地质勘探局完成，监测站精确但昂贵。这意味着可以部署的监测站数量是有限的。为了找到更具成本效益的监控解决方案，【Rohan Menon】和【Ian Vernooy】创建了 [Aquametric，](https://hackaday.io/project/170881-aquametric-cellular-based-stream-monitors)一个简单的水位、温度和电导率测量站。

该设备是围绕粒子电子构建的，具有 STM32 微控制器和 3G 调制解调器。汽车超声波传感器测量水位，热敏电阻测量温度，一对平行铝板用于测量电导率。来自原型的所有数据被输出到一个[实时仪表板](https://aquametric.menon.pro/)。该系统面临的最大挑战来自现场部署。

大自然对我们的想法和电子设备可能相当无情。[Rohan]和[Ian]用 LoRa 做了一些测试，但很快发现地形严重限制了有效范围。电力是另一个挑战，首先用太阳能电池板和锂电池进行测试。这被证明是不可靠的，尤其是在接近冰点的温度下，所以他们决定改用 18 节 AA 电池，并优化电力使用。

安装系统仍然是一个持续的挑战。在河床更宽的部分插入的金属杆最终弯曲(可能来自冰原)，并被碎片覆盖，以至于影响了水位读数。他们随后移动到一个更窄更浅的路段，希望避开碎片，但岩石底部阻止了他们有效地驾驶杆。所以他们把杆子安装在一块钢板上，然后用石头包裹住，使其保持在适当的位置。这也失败了，当它因水位上升而翻倒，淹没了整个传感器单元。令人惊讶的是，它在只有少量湿气进入的情况下存活了下来。

为了 2020 年的黑客日奖， [Field Ready](https://hackaday.com/2020/06/09/the-hackaday-prize-field-ready-is-changing-the-face-of-humanitarian-relief/) 和 [Conservation X Labs](https://hackaday.com/2020/05/28/hackaday-prize-and-conservation-x-labs-issue-design-challenges-to-address-extinction-crisis/) 发起了挑战，这些挑战需要一些仔细的考虑和测试来建造能够在现实世界中生存的东西。那就去黑吧！

The [HackadayPrize2020](https://prize.supplyframe.com) is Sponsored by:[![Supplyframe](img/193ca31946d20fcfa39296cb816a4c50.png)](https://supplyframe.com/)[![Digi-Key](img/4fc24a8a6b4498aecfe987b00009d192.png)](https://www.digikey.com/)[![Microchip](img/8dd361210bbb0e5592c24f87e4e2267e.png)](https://www.microchip.com/)[![Arm](img/7d728b281b85469ef9013d45001f14b4.png)](https://www.arm.com/)