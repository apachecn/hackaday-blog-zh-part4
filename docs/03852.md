# 纸质账本:一种 E-Ink 加密货币股票

> 原文：<https://hackaday.com/2019/08/12/paperledger-an-e-ink-cryptocurrency-ticker/>

很长一段时间以来，电子墨水显示器似乎超出了我们这些低级黑客的能力范围，因为除了点缀这些页面的少数重新利用的 Kindles 之外，我们很少看到珍贵的项目利用这种相对奇异的显示器。但在过去几年里，这种情况发生了变化，我们很高兴地看到黑客们开始让这项不可思议的技术屈从于他们的意志。

一个完美的例子是 PaperLedger，[由[AIFanatic]](https://hackaday.io/project/166908-paperledger) 参加 2019 年 Hackaday 奖的参赛作品。这款无线设备旨在在其 2.9 英寸的电子墨水屏幕上显示各种加密货币的当前价格，并通过内置扬声器提供声音价格警报。它甚至有一个门户网站，用户可以在那里配置硬件或查看更深入的价格信息。

paper ledger[基于 TTGO T5 V2.2 ESP32](https://www.tindie.com/products/ttgo/ttgo-t5-v22-esp32-29-epaper-plus-e-ink-speaker/) ，但看起来[AIFanatic]正在为麻省理工学院的授权项目打造一个新的主板，以解决这一特定应用的一些困扰问题。不幸的是，看起来还没有任何新董事会的照片，但在 Hackaday 上有一个变化的描述。IO 页面显示，大部分工作似乎都在改进对电池供电的支持。

即使你对加密货币不感兴趣，PaperLedger 看起来也像一个神奇的小电子墨水显示器，可以显示你想密切关注的几乎任何东西。该项目的 GitHub 页面上提供了 [GPLv3 授权的固件，因此扩展或完全改变设备的功能对于任何希望这样做并具有 C++工作知识的人来说都不会太难。](https://github.com/AIFanatic/PaperLedger)

在这一点上，我们已经看到几个项目使用[各种 TTGO 板将 ESP32 与显示器](https://hackaday.com/2018/05/23/esp32-boards-with-displays-an-overview/)相匹配，如果你想以最少的麻烦将一些数据[推送到一个小小的 WiFi 屏幕上，这看起来是一个很好的平台。](https://hackaday.com/2019/07/18/live-apollo-11-transcript-on-eink-display/)

The [HackadayPrize2019](https://prize.supplyframe.com) is Sponsored by: [![Supplyframe](img/79a7db035b8a2b6c2b7b0895c45b7de8.png)](https://supplyframe.com/)  [![Digi-Key](img/ba094a14c430ab81591a2abdc54a5363.png)](https://hackaday.io/digikey)  [![Microchip](img/5023ef0b7ff1aee311cba9b54a3ac9fe.png)](https://hackaday.io/microchip)