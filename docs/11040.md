# 电磁干扰的乐趣和利润

> 原文：<https://hackaday.com/2021/08/22/electromagnetic-interference-for-fun-and-profit/>

在机械电表时代，有一个城市传说，有一些“幸运”的电器，一旦插上电源就会让电表倒着走。它可能起源于强容性负载和电表线圈电感之间的相互作用，但对于普通家庭用户来说，这在很大程度上是虚构的。然而，这并不是说电表不能被愚弄去做奇怪的事情，正如特温特大学的一个团队通过发送一些更现代的电表来证明的那样。他们是如何创造这个奇迹的？[来自调光开关](https://research.utwente.nl/en/publications/how-to-earn-money-with-an-emi-problem-static-energy-meters-runnin)的电磁干扰。

阅读[论文](https://ris.utwente.nl/ws/portalfiles/portal/263929998/2021_EMC_Europe_Static_Energy_Meters_Running_Backwards.pdf) (PDF 链接)很明显，这种行为是调光器开关能够相对于电压周期移动电流脉冲相位的结果。交流调光器在 2021 年已经过时，但对于那些不熟悉其操作的人来说，它们的工作原理是只在电源周期的一部分打开。周期时间由调光控制改变。因此，电源过零点和它们的接通点之间的时间相当于电流波形的相移。由于电表在很大程度上取决于这种相位关系，因此它们的性能是可以调整的。也许欧洲商店现在将准备好迎接调光开关的挤兑。

如果你对这些老式调光器感到好奇，[看看它们的一些基本功能](https://hackaday.com/2019/07/14/the-basics-of-scrs/)。

谢谢[多鲁斯]的提示。