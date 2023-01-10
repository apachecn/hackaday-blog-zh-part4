# MIDI 协会宣布 MIDI 2.0 原型

> 原文：<https://hackaday.com/2019/01/19/midi-association-announces-midi-2-0-prototyping/>

MIDI 在 1983 年的 NAMM 展上被引入，作为一种将各种电子乐器连接在一起的手段。从那以后，我们最喜欢的五针 DIN 被塞进了 Radio Shack 键盘、MPC、synths、eurorack 模块和 Daw。标准基本没变。当然，我们有 MIDI SysEx 消息来配置 MIDI 设置的各个组件，但在其核心，MIDI 没有改变，因为它是作为 1 MHz 下运行的 8 位微控制器的电流环路串行协议而设计的。

现在，在 2019 年 NAMM 展之前，MIDI 制造商协会(MMA)联合 AMEI，日本 MIDI 协会，[宣布推出 MIDI 2.0](https://www.midi.org/articles-old/the-midi-manufacturers-association-mma-and-the-association-of-music-electronics-industry-amei-announce-midi-2-0tm-prototyping) 。新功能包括，“自动配置、新的 DAW/web 集成、扩展的分辨率、增强的表现力和更紧凑的时间安排”。它将保持与 MIDI 1.0 设备的向后兼容性。

像第一个 MIDI 规范的发布一样，这个新的倡议是乐器制造商之间的一个合资项目。该新闻稿上的公司阵容如下:Ableton/Cycling '74，Art+Logic，Bome Software，Google，imitone，Native Instruments，Roland，ROLI，Steinberg，TouchKeys，和 Yamaha。

这不是 MIDI 2.0 规范的官方声明。这是“原型制作”阶段，制造商按照设想实施 MIDI 2.0 规范，编写一些文档，确定新徽标的外观，并设计自我认证流程。原型制作预计将持续到 2019 年，届时最终的 MIDI 2.0 规范将在 MIDI 协会网站上发布。

就硬件黑客而言，如果你没有做任何新的事情，你现有的 MIDI 实现不应该有任何改变。毕竟它应该是向后兼容的。新规范将允许更大的表达范围和“更紧密”的时序，这可能表明 MIDI 的波特率(31，250 波特+/- 1%)可能会发生变化。对于现存的最后一个老式物理层，有一些有趣的事情在等待着，我们迫不及待地想看看它会产生什么。