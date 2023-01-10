# Odyssey 是一台 X86 计算机，为旅行打包了一个 Arduino

> 原文：<https://hackaday.com/2020/08/07/odyssey-is-a-x86-computer-packing-an-arduino-along-for-the-trip/>

我们喜欢 Arduino 对于专注任务的简单性，我们喜欢 Raspberry Pi GPIO 引脚如何打开通往广泛外设世界的大门，我们喜欢英特尔 x86 指令集的软件生态系统。一些产品成功地将所有这些结合到一个紧凑的包中，这很好，我们欢迎最近添加的 [Seeed Studio 的 Odyssey X86J4105](https://www.seeedstudio.com/ODYSSEY-X86J4105800-p-4445.html) 。

[Ars Technica] [最近浏览了一遍](https://arstechnica.com/gadgets/2020/08/review-odyssey-x86j4105-a-mini-pc-for-makers-and-builders/)，发现从一台小型联网计算机的角度来看，它令人印象深刻，但他们没有深入挖掘该产品对制造商友好的一面。我们可以通过查看[产品文档](https://wiki.seeedstudio.com/ODYSSEY-X86J4105/)来了解一些有趣的细节。这块板比树莓 Pi 大，但是它的 [GPIO 管脚的布局](https://wiki.seeedstudio.com/ODYSSEY-X86J4105-GPIO/)和 Pi 上的完全一样。一些帽子可以直接插入，消除所有的电气集成，只留下 ARM 与 x86 的软件问题。不适合 CPU 控制的 GPIO 的任务(如产生可靠的 PWM)可以卸载到板载 Arduino 兼容微控制器。它围绕 SAMD21 芯片构建，类似于 Arduino MKR 和 Arduino Zero，但[引脚排列似乎不匹配](https://wiki.seeedstudio.com/ODYSSEY-X86J4105/#pinout-diagram)任何流行的 Arduino 外形。

Odyssey 不是第一台具有 GPIO 引脚和板载 Arduino 助手的 x86 单板计算机(SBC)。例如，LattePanda 在过去几年中一直在执行那个游戏计划(不包括树莓派图钉布局)。自从他们的 Kickstarter 起源以来，我们就一直关注着他们的[，我们还展示了这里](https://hackaday.com/2015/12/03/windows-10-on-a-tiny-board/)和那里[的创造性应用](https://hackaday.com/2019/09/23/magnets-make-this-panda-move/)。LattePanda 目前的产品是围绕从凌动到酷睿 m3 的英特尔 CPU 构建的。奥德赛的赛扬大约在这个范围的中间，SAMD21 比 LattePanda 上的 ATmega32U4 (Arduino Leonardo)更有能力。我们总是喜欢在市场上看到更多的选择，让我们找到合适的权衡来匹配给定的项目，我们期待史诗般的旅程即将到来。