# 向 FPGA 挑战

> 原文：<https://hackaday.com/2020/10/11/throwing-down-the-fpga-gauntlet/>

Gauntlet 是一款著名的街机游戏，从 1985 年开始，有许多续集和端口到更现代的架构，如 Xbox 和 GameCube。由于它的受欢迎程度和相对年龄，最初的拱廊橱柜有很好的文档记录，其示意图可在网上获得。在发布的时候，它被认为是雅达利有史以来开发的最复杂和最雄心勃勃的硬件。在只能被描述为绝对热爱的工作中，[Alex]在 Pipistrello FPGA 板上重建了街机硬件。

该项目实际上可以玩《挑战》、《挑战 II》和《维护者 II》，因为它们都运行在相同的硬件上。支持四个操纵杆，因此最多可以有四个玩家玩，尽管 EEPROM 是在 RAM 中模拟的，因此当设备断电时，高分会被重置。FPGA 几乎空间不足，无法完全容纳所需的 SRAM。因此需要 SRAM 扩展子板；我们最喜欢的紫色 PCB 制造商的快速电路板运行解决不了任何问题。

回购中有一篇[令人难以置信的文章](https://github.com/d18c7db/Gauntlet_FPGA/tree/master/doc)详细介绍了该系统、其工作原理以及调试过程。该项目还包括 TMS5220 语音合成处理器的完整模拟，因为 Gauntlet 是第一台带语音合成器的投币游戏机。获得正确的视频是特别棘手的，需要几次尝试才能让调色板和动作看起来正确。因为[亚历克斯]没有原始的戈特莱特拱廊橱柜，他们不得不与 MAME 凑合。在编写测试以确保 FPGA 正常工作后，MAME 仿真和 FPGA 输出之间存在差异。为了帮忙，[科林·戴维斯]前来救援。在[Colin]连接了一个加载了运动测试的原始 Gauntlet Arcade PCB 后，测试显示 FPGA 具有正确的行为。

在开发过程中,[Alex]实际上在 ISIM 模拟了游戏的几帧(每帧 90 秒或者游戏中每一秒 90 分钟)。使用 ISIM 可以让他们将系统状态与 MAME 进行比较，并更快地验证设计，因为他们可以更好地检查不同模块的交互工作。他们使用一个聪明的技巧，在几秒钟后从 MAME 获取状态，启动 FPGA 状态，为自己节省了几个小时的模拟时间。

如果你想进入老硬件风格的街机游戏开发，试试基于浏览器的 8bitworkshop IDE 吧。或者从这个[可爱的迷你 CRT 街机柜的范围和尺寸小一点的东西开始。](https://hackaday.com/2012/03/16/crt-vector-graphics-arcade-game-built-from-an-fpga-board/)

 [https://www.youtube.com/embed/7A2k7wLUSUU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/7A2k7wLUSUU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[Alex]发送此邮件！