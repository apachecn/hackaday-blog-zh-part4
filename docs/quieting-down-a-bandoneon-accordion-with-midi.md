# 用 MIDI 让手风琴演奏安静下来

> 原文：<https://hackaday.com/2020/04/13/quieting-down-a-bandoneon-accordion-with-midi/>

被称为探戈手风琴的 bandoneon 是一种在公寓范围内练习的相当响亮的乐器，可能会导致一些邻里纠纷。[HLB]喜欢演奏他的吉他，但是考虑到他的邻居，他想找一种方法把音量调小一点。他决定用 Arduino 和 MIDI 来解决这个问题，而不是建造一个完整的隔音室。

像所有的手风琴一样，手风琴的工作原理是将空气从手动充气的风箱中推出，穿过一系列簧片，每个簧片由一个阀门机构打开和关闭。[HLT]通过连接一个磁铁，将每个阀杆变成一个简单的开/关开关，在每排阀门旁边的长定制 PCB 上安装霍尔效应传感器。霍尔效应传感器连接到 I2C I/O 扩展器 IC，后者连接到 Arduino Nano，乐器的每一侧各有一个，通过串行发送 MIDI 信息。所有的东西都被安装在一个看起来很旧的仪器里，用 Blu Tack 来避免做很多永久性的修改。

bandoneon 在没有永久修改的情况下仍能正常工作，所以用 MIDI 演奏时——只是风箱没有充气。这意味着[HLB]不能在演奏时调节 MIDI 速度(响度)，他承认这是一个限制，但总比根本不演奏好。然而，他指出，如果我们想在 midi 输出中增加力度，而不考虑邻居关系，他可以在风箱内增加一个压力传感器。在音频输出方面，[HLB]建立了一个小型的独立合成器，带有运行 FluidSynth 的 Odroid SBC 和 HiFi shield。

我们认为这是对一个实际问题的一个执行良好的解决方案，没有在技术方面做得过多。所有细节，包括 KiCad PCB 文件和 Arduino 代码，都在 Github 上，因此可以随意使用和修改它，以建立自己的音乐天赋。

几乎每种乐器都可以输出 MIDI，在过去的几十年里，它实际上已经成为大型建筑大小的管风琴的核心部分。