# 2022 年 Hackaday 奖:BinPal 是一个方便的回收提醒

> 原文：<https://hackaday.com/2022/06/11/hackaday-prize-2022-binpal-is-a-convenient-recycling-reminder/>

虽然在路边收集可回收物很方便，但它确实需要你跟踪哪种废物是在什么时候被收集的:错过两周一次的纸张收集，你很快就会发现自己储备了四周的盒子和报纸。当[Dominic Buchstaller]的纸板堆到他的天花板时，他决定采取行动，为自己做一个 [BinPal:一个冰箱磁铁，它可以帮助你记住什么时候拿出哪个垃圾桶。](https://hackaday.io/project/185708-binpal-the-friendly-recycling-reminder)

这个简单而有效的 BinPal 的核心是一个 ESP32 板，它连接到 Google Apps 脚本并从 Google Calendar 中检索取件时间表。如果四种垃圾中的一种需要被收集，它的图标会在 LCD 屏幕上高亮显示。用户可以按下一个触摸感应按钮来确认箱子已经被取出用于拾取；如果到晚上 8 点还没有完成，显示器的背光开始闪烁，作为额外的提醒。

该设备的外壳由激光切割的胶合板制成，内部粘有几块强磁铁，以确保 BinPal 牢固地附着在冰箱上。本着真正的循环利用精神，[Dominic]只用他零件箱里的零件来制作 BinPal。然而，这些器件都很容易在网上获得，并且通过项目的 Hackaday.io 页面上提供的完整原理图和代码，应该很容易使设计适应不同的硬件平台。

[Dominic]的设计灵感来自于几年前我们推出的一款闪烁的 LED 家务提醒灯。你也可以通过[重复使用 Kindle 的电子纸显示屏](https://hackaday.com/2013/04/01/kindle-weather-and-recycling-display/)来制作家务提醒。

[hack adayprize 2022](https://prize.supplyframe.com)主办单位:[![Digi-Key](img/e7d13a315fd6226594212ca8f8762832.png)](https://www.digikey.com/)[![Supplyframe](img/fdb8a432506edeeafacfef227b3d3b33.png)](https://supplyframe.com/)