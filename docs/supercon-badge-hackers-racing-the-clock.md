# 超级徽章黑客争分夺秒

> 原文：<https://hackaday.com/2018/11/06/supercon-badge-hackers-racing-the-clock/>

在 Hackaday Superconference 周末结束时，我们在主舞台上举行徽章黑客仪式，邀请任何使用徽章做过任何事情的人上台展示他们的工作。是的，哪怕只是一个闪烁的 LED！这是一个巨大的快乐，不仅看到人们相信我们的话，并提出闪烁的 led，但在房间里的社区欢迎这些入门者欢呼硬件黑客。然而，在仪式之前，徽章黑客们用烙铁武装起来，靠咖啡因来补充能量，进行了大量疯狂的工作。人们在一个专注的周末能完成多少事情总是令人惊讶的。

在我们之前对 super co badge hacking 的[概述中，为了方便起见，【](https://hackaday.com/2018/11/04/green-led-means-go-for-supercon-badge-hacking/) [macegr](https://twitter.com/macegr) 只有一个容纳 USB 到串行转换器的扩展板。从那以后，它已经成长为一个 LED 阵列，到晚上结束时，成为康威生命游戏的一个实现。对于一个不起眼的串行转换器来说，这是一个很大的进步！说到方便的端口，[Drew]和[Mike L]在他们的徽章上加了一个 PS/2 键盘端口。然而，功能只是故事的一半。另一半是他们的足智多谋，使用从 Supercon 与会者的礼品袋中收集的零件。

 [![macegr progression](img/d4761ed123b0d19240dc16ae97a195e3.png "macegr progression")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/11/macegr-progression.jpg?ssl=1)  [![MikeL PS2](img/3d3fdebe5ca234c9f7688528ee3cbc4f.png "MikeL PS2")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/11/mikel-ps2.jpg?ssl=1) 

“端口”一词的另一个意思是，[Marcel]为他的 Gigatron TTL 计算机移植了一个模拟器，在他的徽章上运行。[Nick]跳入他徽章上的 Z80 模拟器，徽章上有一个由[Tim]设计的[外壳](https://hackaday.io/project/162134-hackaday-superconference-2018-badge-enclosure)。[Nick]的目标是让 SuperCalc(原始电子表格程序之一)运行起来。[邵]努力把他的 XORLib 项目移植到他的徽章上。

 [![Gigatron](img/f30752eb33b74376ee6ab78233436330.png "Gigatron")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/11/gigatron.jpg?ssl=1)  [![NickSuperCalc](img/c3816605d9d61add90cc3ed4cfc54f76.png "NickSuperCalc")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/11/nicksupercalc.jpg?ssl=1) 

多个项目向徽章添加了音频输入。[交换文件]将一个麦克风输入一个少年，这个少年命令徽章将音乐和丰富的 led 一起显示在屏幕上。[Scott]走了一条不同的路线——音频信号被传送到戴在皮肤上的电极，使佩戴者能够透过皮肤听到声音。我们甚至还有[ [Tucanae47](https://twitter.com/tucanae47) 带来的 [MATRIX 语音](https://www.matrix.one/products/voice)麦克风阵列。

 [![audio visualizer badge](img/3208369e92d8cba9d171ecbeb10acc24.png "audio visualizer badge")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/11/audio-visualizer-badge.jpg?ssl=1)  [![skin electrodes](img/526cc588f2f6099dc4128ad34cffc4fd.png "skin electrodes")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/11/skin-electrodes.jpg?ssl=1)  [![MATRIX Voice badge hack](img/20ab5538827837e12095070d0cb7e6fa.png "MATRIX Voice badge hack")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/11/matrix-voice-badge-hack.jpg?ssl=1) 

在 badge audio 的输出端，制造了一些非常棒的噪声源。[Todd] [将他刚刚在“逻辑噪音:你自己的原始合成器试验板”研讨会上学到的东西应用到徽章黑客中。[托尼]和[丹]建造了一个](https://hackaday.io/project/162184-tune-the-hard-way-via-logic-noise-supercon-18)[相控扬声器阵列](https://hackaday.io/project/162193)，旨在帮助视障人士。和[ [EdjeElectronics](https://twitter.com/EdjeElectronics) ]曲柄徽章音乐音量高达 11 与放大器驱动扬声器几乎一样大的徽章本身。

 [![Todd Synthesizer](img/2c6296703bbb4b190ef2285e01ba4890.png "Todd Synthesizer")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/11/todd-synthesizer.jpg?ssl=1)  [![ShredPhase](img/942e2dfc4a7fcae064aae866b86fd318.png "ShredPhase")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/11/shredphase.jpg?ssl=1)  [![EdjeElectronics](img/62ff275b43966d0e7a3b5de6383c1cf2.png "EdjeElectronics")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/11/edjeelectronics.jpg?ssl=1) 

相当多的项目使用徽章的扩展端口与有趣的硬件接口，正如徽章设计的意图。[Ben]展示了一个徽章，乍一看，是运行 Linux 发行版的。然后他会解释自己的错觉:贴在徽章上的黑匣子是树莓皮外壳，徽章是终端。[迭戈]的[制造者 Muscle](https://www.kickstarter.com/projects/deezmaker/maker-muscle-worlds-first-customizable-actuator-fo) 几乎可以被任何控制器控制，现在这个列表包括徽章。[ [乔迪](https://0xdec.im/) ]认为计算能力越强越好，所以他的 badge 扩展板现在是 1bitsy 板、ATMega32 板和 RISC V 板的家。仅仅是让它们共存就足够令人印象深刻了。在检查之前概述中提到的另一个团队时，[[摩根](https://hackaday.io/captain.morgan)和[[本](https://twitter.com/im889)]在仪式前一个小时建立并运行了他们的无线网状网络。(时间充裕！)网络上的徽章都配备了一个[极简的 ESP32 插件](https://hackaday.io/project/161906)和大量的软件魔法。

 [![BenLinuxPi](img/cac04b20f0772a0838877d56f9e55381.png "BenLinuxPi")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/11/benlinuxpi.jpg?ssl=1)  [![DiegoMakerMuscle](img/d7964a193957b788ba5848b3d3ae4e13.png "DiegoMakerMuscle")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/11/diegomakermuscle.jpg?ssl=1)  [![JordiParty](img/5973be628077d205ceac71cf13625e6b.png "JordiParty")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/11/jordiparty.jpg?ssl=1)  [![BenMorganMeshNet](img/f341885ad62b089f9bd1a5151b0f5dbe.png "BenMorganMeshNet")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/11/benmorganmeshnet.jpg?ssl=1) 

周末结束时，所有这些项目——以及更多项目——结果如何？在徽章破解仪式上自己看吧。我们很高兴看到今年所有这些巨大的徽章黑客，我们邀请您加入我们的下一次黑客日超级会议。

 [https://www.youtube.com/embed/WCLlz_taeQk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=377&wmode=transparent](https://www.youtube.com/embed/WCLlz_taeQk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=377&wmode=transparent)

