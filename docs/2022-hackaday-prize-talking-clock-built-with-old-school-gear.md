# 2022 年黑客日奖:用老式设备制造的会说话的时钟

> 原文：<https://hackaday.com/2022/08/16/2022-hackaday-prize-talking-clock-built-with-old-school-gear/>

如果你愿意，任何智能手机或笔记本电脑都可以成为一个会说话的时钟。然而，我们认为来自[Marek wice k]的这种构建更有趣，它使用离散的老式芯片以传统的方式完成工作。

这项工作始于[Marek]修补 65C02 CPU，给它一个 EPROM、一些 RAM 和一些逻辑 ic，以创建功能类似于现代微控制器的东西。它被称为 *6502 复古控制器板*。慢慢地，这个项目随着各种附加模块的增加而扩展，就像给 Arduino 增加护盾一样。

在这种情况下，[Marek]扩展了 6502 供电板，增加了一系列 7 段显示屏，以及一个 RTC 来保持准确的时间。然后添加了一个经典的 SP0256-AL2 语音合成芯片，使系统不仅可以显示时间，还可以大声读出时间。另外，它不仅能告诉你小时、分钟、星期和日期，还能根据需要阅读各种科幻小说中的引言。

像大多数 80 年代的语音合成器一样，输出是机器人式的，有点难以解析。然而，这也是它与今天会说话的虚拟助手不同的魅力所在。

 [https://www.youtube.com/embed/TW14inHkuYU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/TW14inHkuYU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2022](https://prize.supplyframe.com) is Sponsored by:[![Digi-Key](img/e7d13a315fd6226594212ca8f8762832.png)](https://www.digikey.com/)[![Supplyframe](img/fdb8a432506edeeafacfef227b3d3b33.png)](https://supplyframe.com/)