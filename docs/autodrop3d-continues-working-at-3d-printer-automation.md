# Autodrop3D 继续致力于 3D 打印机自动化

> 原文：<https://hackaday.com/2019/06/06/autodrop3d-continues-working-at-3d-printer-automation/>

不幸的是，3D 打印机大部分时间都处于闲置状态，等待人类移除完成的打印或等待下一次打印开始。黑客将这种低效视为设计更好方法的公开邀请，我们已经在这些页面上看到了一些创新的想法。一些已经被放弃了，但是其他的还在继续。在 Maker Faire Bay Area 2019 上，我们有机会重访一个被展示为 Autodrop3D 的[。](https://autodrop3d.com/)

[![](img/a794096c08421df72605de0e544aaa8c.png)](https://hackaday.com/wp-content/uploads/2019/06/Autodrop3D-at-MFBA19-big-and-small-600x600.jpg) 我们看到了一个更早的迭代[进入了我们 2017 年的 Hackaday 奖](https://hackaday.com/2017/06/24/hackaday-prize-entry-a-3d-printer-management-system/)，看到基本思想在过去几年中的发展是令人着迷的。该系统最明显的组成部分是他们的打印喷射系统，大大提高了鲁棒性。因为该机构修改了打印床并增加了大量质量，所以它最适合于 delta 打印机，因为它们的打印床保持静止。这个概念可能适用于打印床只需沿 Z 轴移动的打印机，但目前团队仍专注于增量。Maker Faire 上展示了两种实现:一种是基于 SeeMeCNC RostockMAX v4 的大型实现，另一种是基于 [Monoprice Mini Delta](https://hackaday.com/2017/08/21/monoprice-mini-delta-review/) 的小型实现。

弹射系统本身足够新颖，但硬件只是端到端 Autodrop3D 视觉的一部分。他们的[完整软件管道](https://github.com/autodrop3d)从基于网络的 CAD 开始，到集成切片，到打印队列管理，然后 g 代码被送入配备有喷射系统的打印机。

我们钦佩那些不断努力将愿景变为现实的发明家，我们期待下次与这个团队见面时看到新的东西。与此同时，如果你喜欢自动打印弹出机制的想法，但想要更多的卡通风格，[看看 MatterHackers](https://hackaday.com/2015/06/06/automatic-print-ejector-for-all-3d-printers/) 的这项发明。