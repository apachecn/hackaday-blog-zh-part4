# 磁力曲棍球游戏用的是 555

> 原文：<https://hackaday.com/2022/04/06/magnetic-hockey-game-uses-a-555/>

我们喜欢 Hackaday 的好项目，尤其是让我们想拿起它并尝试一下它对我们自己有什么好处的项目。当我们看到这样一个项目，并发现它包含一个芯片来统治他们所有人(或者称为 NE555 定时器)，我们的集体奖杯充满了喜悦。因此[【安德鲁·芬特姆】的磁力曲棍球项目](https://hackaday.io/project/184732-accelerator-22-science-fiction-air-hockey)无疑触动了我们所有的按钮，因为这是一个表面上类似于空气曲棍球台的游戏，其中磁力冰球由手持电子球棒加速。

这些蝙蝠看起来非常高科技，但实际上却出奇的简单。每一个都包含一个霍尔效应传感器，它会触发 555，我们希望它是作为单稳态电路连接的，这又会触发一个 MOSFET，它会在一段设定的时间内给电磁铁供电。冰球是一个磁铁，因此当霍尔传感器检测到它时，它会被电磁体高速射出。结果是一个快节奏的游戏，比传统的空气曲棍球有额外的优势，老实说，我们很想尝试一下。在休息下面的视频里可以看到。

当然，如果在这个半导体短缺的时代，你的预算不是一个而是两个芯片，[你总是可以尝试传统的桌子](https://hackaday.com/2019/08/26/air-hockey-table-is-a-breeze-to-build/)。

 [https://www.youtube.com/embed/e8KzBefac_Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/e8KzBefac_Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

