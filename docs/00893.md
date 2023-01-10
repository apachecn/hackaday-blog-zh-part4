# 为你的硬币电池提供更好的充电器

> 原文：<https://hackaday.com/2018/10/09/a-better-charger-for-your-coin-cell-batteries/>

可充电硬币电池非常适合你所有的小项目。它们看起来就像普通的硬币电池，但令人震惊的是，你可以给这些小家伙充电。它们可以输出合理数量的电流，而且体积很小。这正是你的 Arduino 智能手表所需要的，或者这些天孩子们正在做的任何事情。

但是如果这些电池是可充电的，你需要一个充电器。这就是[Jon]的 Hackaday 奖参赛作品派上用场的地方。这是 LIR2032 和其他充电电池的小型廉价充电器。它比电池本身大不了多少，可以直接插入 USB 接口。我们永远也不会知道为什么这还不是一个产品。

这款纽扣电池充电器的电路由 MCP73831 构建而成，这是一款不错的单电池、锂离子和锂聚合物充电管理控制器。在标准的‘我只需要阅读数据手册的第一页’配置中，这种芯片可以将 500 mA 放入一个电池中。标准的可充电硬币电池只有 40 毫安时的容量，所以在 1C 时你有足够的余量。

该项目的总成本是三块板不到 8 美元，一块板的 BOM 成本是 2 美元。如果你知道如何焊接，三个这样的充电器要 14 美元，相比之下，一个标准的现成充电器要 20 美元。建造这个比购买同等产品更便宜。难以置信，但却是真的。

The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)