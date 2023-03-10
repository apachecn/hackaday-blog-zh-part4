# 只需一点热量，打印的零件就能处理真空工作

> 原文：<https://hackaday.com/2022/09/13/with-a-little-heat-printed-parts-handle-vacuum-duty/>

我们不必告诉普通的黑客读者，桌面 3D 打印已经为我们的社区带来了变革，但这项技术对科学界的影响可能不那么明显。正如【Pierce Mayville】、【Aliaksei Petsiuk】、【Joshua Pearce】在 [*为
真空系统*进行的 3D 打印聚丙烯部件的热后处理中所解释的那样，打印塑料部件的使用，尤其是基于开源设计时，可以导致科学硬件生产成本的大幅降低。](https://www.mdpi.com/2504-4494/6/5/98)

更具体地说，作者希望检查在真空中使用 3D 打印组件的情况。用基于细丝的打印机生产的零件往往是多孔的，因此，不适合于需要抽至低于一个大气压的配件或适配器。该论文继续解释说，有涂层可以用来密封印刷部件，但它们可以在负压下除气。

该团队提出的解决方案非常简单:在 Lulzbot Taz 6 上用聚丙烯打印出他们想要的零件后，他们只需用标准的消费者热枪击打它们。当温度设置为大约 400°C 时，不到一分钟的时间，表面就呈现出光滑的外观——结果让我们想起了用丙酮蒸汽平滑的 [ABS 印刷。](https://hackaday.com/2013/03/23/smoothing-3d-prints-with-acetone-vapor/)

[![](img/ec3bf3f2e44a667bc9eed17a6fdb951d.png)](https://hackaday.com/wp-content/uploads/2022/09/vac3dp_detail.jpg)

As the part is heated, the surface texture visibly changes. The smoothed parts performed far better in vacuum testing.

除了热处理之外，该团队还在切片机设置中增加了填充重叠度。最终结果是，以高重叠印刷然后热处理的部件能够可靠地处理低至 0.4 毫托的压力。虽然这篇论文承认，用热风枪手动烹饪你的打印部件并不是生产真空部件的理想解决方案，但这肯定是一个有希望的开始，值得进一步研究。