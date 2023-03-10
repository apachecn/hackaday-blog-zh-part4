# 为了赞美 DT830，这款非凡的乐器你可能不知道它是什么

> 原文：<https://hackaday.com/2020/09/24/in-praise-of-the-dt830-the-phenomenal-instrument-you-probably-dont-recognise-for-what-it-is/>

如果我们必须对 Hackaday 读者中比例最高的电子工作台设备进行猜测，它不会是 Rigol 的预算示波器，也不会是 TS100 这样受欢迎的便携式烙铁。相反，我们猜测这是一个万用表，甚至不是最完善的一个。

DT830 是中国制造的 3.5 位数字万用表，价格低得惊人。不到一个像样的汉堡就能让你买到一个一眼就能认出来的塑料盒子，里面有一个笨重的旋转范围选择开关，也许还有一个某种晶体管或元件测试器的插座。确保安装了 9 伏电池，插上这对测试引线，您就可以进行几乎任何日常电气或电子测量了。几十年来，它们已经以这样或那样的形式存在，并且已经成为无数赠品和亏本优惠的主题，所以有理由猜测你在某个地方会有一个。据我所知，我有三个，它们是很棒的移动工具，并且已经证明了它们惊人的可靠性。

## 说服你将是一件困难的事情

[![An undervalued instrument, by my estimation.](img/73fb87e34fe989c58016134a82b80d9f.png)](https://hackaday.com/wp-content/uploads/2020/07/dt830-yellow.jpg)

An undervalued instrument, by my estimation.

如果你在上流社会谈论 DT830，迎接你的可能是嗤之以鼻的嘲笑。不难找到这样的评论:把一个电表拆下来，与一个更贵的电表进行比较，并毫不奇怪地发现这个昂贵的电表质量更好。

当然，只需几美元，你就能得到一个不会永久使用的开关和可能不太符合规格的高压隔离。但我将对 DT830 提出一种不同的看法，这可能会让你们中的一些人感到惊讶:对我来说，它是一款现代经典，一款性价比极高的乐器。因为这种袖珍电表不仅能测量电压、电流和电阻，而且测量准确、可重复，与以前相比，这是一种更好的设备。

三十年前，数字万用表是一个昂贵的东西，大多数万用表仍然是模拟的。因此，便宜的万用表总是一个小型的袖珍模拟装置，非常便宜的万用表可能会非常糟糕。读数的准确性和可重复性不是他们的强项，虽然我[是模拟万用表的狂热粉丝](https://hackaday.com/2017/11/08/why-you-shouldnt-quite-forget-the-moving-coil-multimeter/)，但当谈到发现调整模拟电路的下降和趋势时，即使是我也找不到理由来称赞便宜的万用表。相比之下，DT830 通过高阻抗输入提供可靠和准确的读数，这是我在 1985 年愿意付出很多的东西。

## 那场演出绝非侥幸

[![An ICM7106 epoxy blob on a 40-pin DIP-shaped PCB](img/32b93d8d86875243efb109213c91ad85.png)](https://hackaday.com/wp-content/uploads/2020/07/dt830-40pin-7106.jpg)

An ICM7106 epoxy blob on a 40-pin DIP-shaped PCB in this roughly 18-year-old DT830

那么，考虑到在英国酒吧里它的价格比一品脱啤酒低得多，这么便宜的仪器是怎么做到的呢？答案是，站在巨人的肩膀上。我的同事 Anool Mahidharia 在 2017 年提供了答案，当时他看了看 Intersil 71XX 系列集成电路；原型 DT830 包含一个 [ICM 7106](https://www.maximintegrated.com/en/products/analog/data-converters/analog-to-digital-converters/ICL7106.html/tb_tab0) 3.5 位数字面板仪表芯片，其根源在于一个更具排他性的行业阶层。

(尽管市场上有大量更新、更完善的万用表芯片，但我惊讶地发现，没有一个能进入我打开的电表。)

ICM 7106 是基于 Intersil 在 1977 年生产福禄克第一台便携式数字万用表 8020A 型的工作。

[![Google hasn't found any ICM7106 conterfeiters!](img/68db3a2d08c1b399d4a293bcf2f1442f.png)](https://hackaday.com/wp-content/uploads/2020/07/dt830-counterfeit-7106-search.jpg)

Google hasn’t found any ICM7106 conterfeiters!

因此，你无法接近这种昂贵的仪表的物理设计或组件质量，但你受益于使其祖先成为 20 世纪 70 年代非常好的仪器的技术。双斜率积分 ADC 和精密基准电压源与许多昂贵得多的电表中的相同，这使得您可以信赖价格低廉的 DT830 的读数。对于你可能认为是垃圾的东西来说还不错！

如果从这个故事中可以得到什么的话，这是半导体制造力量的一个非常真实的展示。假设它已经通过了可接受的工厂质量保证，每一个 7106 都和任何其他 7016 一样好，从 Intersil 在 20 世纪 70 年代制造的第一个 7106，到藏在我廉价仪表的环氧树脂滴下的来历不明的芯片。制造商可以克扣电表中的所有其他组件，但假设没有钱来伪造一个 43 年前的芯片，这个芯片很久以前就离开了其优质产品阶段，多年来由许多来源制造，他们不能克扣为其供电的芯片。要成为 ICM7106，它必须具有与 20 世纪 70 年代的原版相同的功能，因此我的廉价电表仍然具有更高质量的一些重要内容。

那么就用 DT830 万用表。它可能是一堆垃圾，但却是一堆好得惊人的垃圾。我，向它致敬。