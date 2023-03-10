# 双端口内存和 Raspberry Pi 联手打造复古控制台多卡

> 原文：<https://hackaday.com/2018/07/26/dual-port-memory-and-raspberry-pi-team-up-for-retro-console-multicart/>

重温我们个人过去美好的时光中使用游戏机的体验是很有力量的，特别是数百个小时操作廉价操纵杆积累的触觉记忆，或者插入游戏盒的声音和感觉。模拟器有他们的位置，但是他们在怀旧部门远远达不到时期正确的硬件。

这并不是说复古装备在可用性方面不能使用一点帮助，这也是为什么【斯科特·m·贝克】为他的雅达利 5200 打造[这款树莓 Pi 多弹药筒的原因。这个想法是为了保持卡带界面的体验，而不必为他想玩的所有游戏保留成堆的卡带。[Scott]利用了他在为自制 PC/XT](http://www.smbaker.com/pi-powered-atari-5200-multi-rom-cartridge-multicart)制造[虚拟软驱时使用的方法:双端口内存。IDT7007 是一个 32k 芯片，位于 Atari 5200 和 Raspberry Pi Zero 之间，可以由两个系统寻址；Pi 将 ROM 映像写入内存，控制台读取它们。他必须处理一些繁琐的细节，如芯片选择逻辑和处理墨盒互锁信号，更不用说内存芯片的逻辑电平和 Pi 的逻辑电平之间的电压差了。复古玩法占据了下面视频的第一部分；跳到 6:45 了解构建细节。](https://hackaday.com/2018/05/04/making-vintage-computing-easy-the-hard-way/)

我们唯一的吹毛求疵就是试图把所有东西都塞进一个旧弹药筒里。这对于复制触觉体验至关重要，虽然我们不认为我们已经走得那么远，以[注射成型定制墨盒](https://hackaday.com/2012/12/15/adventures-in-moldmaking-and-making-your-own-enclosures/)来容纳所有没有任何突起的东西，但我们可能已经 3D 打印了一个定制墨盒。不过，最终它不会对完成的项目有太大影响，我们欣赏新旧技术的结合。

 [https://www.youtube.com/embed/xn7xKqfmdIc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/xn7xKqfmdIc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

