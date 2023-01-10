# 从艺术装置建筑中学到的教训

> 原文：<https://hackaday.com/2019/07/11/lessons-learned-from-an-art-installation-build/>

艺术装置是一个有趣的行业，越来越多的倾向于在他们的创作中加入电子或机械元素。与更主流的工程相比，这一领域的工作方式通常有很大不同。[Jan Enning-Kleinejan]参与了一个名为*Prendre la parol，*T2 的装置作品，并分享了从这次经历中获得的经验教训。

该装置由一系列独立的雕像组成，每个雕像都装有 LED 灯。此外，每座雕像都装有一个模块，当它检测到附近有游客时，就会发出声音。最初的设计使用主电源，但是对于这种特殊的安装，将需要电池电源。

Arduinos，USB 电源组和超声波测距仪都被扔进组合中来完成这项工作。DFplayer 模块用于运行声音，Grove 系统部件用于快速轻松地连接一切。虽然这对于产品设计来说是一个奇怪的选择，但艺术项目严重依赖快速原型工具是很常见的。它们使没有经验的用户能够快速有效地完成一个低成本的好项目。

[Jan]很好地解释了项目中面临的一些陷阱，并报告说该装置在 6 个月内几乎完美地运行，每天运行 8 小时。我们喜欢在这些地方看到好的艺术作品，我们可能会有一些符合你口味的东西——无论你是喜欢[口琴](https://hackaday.com/2018/12/13/the-battle-between-robot-harmonica-and-machine-finger-rages-on/)、[木耳](https://hackaday.com/2019/06/03/artistic-attempt-to-send-digital-signals-via-fungus/)还是[马尔可夫链](https://hackaday.com/2018/12/17/bit-installation-combines-art-markov-chains/)。