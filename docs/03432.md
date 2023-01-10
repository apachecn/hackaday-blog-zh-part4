# 复古完美的四个筹码

> 原文：<https://hackaday.com/2019/07/10/four-chips-to-retro-perfection/>

这些年来，我们已经看到许多人从头开始构建计算机。它总是很棒，[但是这一个拿蛋糕](https://hackaday.io/project/159973-z80-mbc2-4ics-homemade-z80-computer)。我这么说不仅仅是因为丝印上有一个可爱的小“Z80 Inside”标志。这是一台四个集成电路的 Z80 电脑，一个小小的主板，而且[Just4Fun]参加了今年的 Hackaday 奖。

这个单板电脑只有四个芯片，最重要的是 CMOS Z80 CPU。这与在 TRS-80 和 ZX 光谱中发现的 CPU 相同，这两个都是早期计算的经典。除了 PCU，还有一个 128 千字节随机存取存储器的东芝 SRAM。一个 74HC00 被扔进混合物中用于粘合逻辑，其他一切都通过一个特别编程的 ATMega32A 发生。最后一个芯片为 CPU 提供了通用 I/O 子系统、EEPROM 和 4/8MHz 时钟。

这四个芯片确实是一台全功能计算机所需要的全部，但是您可以用这块小小的主板做更多的事情。[有一个 uCom 板](https://hackaday.io/project/159973/log/164037-ucom-is-out)，或者基本上是一个“透明的”USB 转串行仿真器，允许您将十六进制文件上传到板上。当然，这意味着你也可以把它连接到一个终端上，[，有了 FuzixOS，Z80 就有了 Unix。](https://hackaday.io/project/159973/log/163704-fuzixos-preview-unix-for-z80)这是逆向计算的一大奇迹，也是当今改造旧电脑的最佳方式之一。

The [HackadayPrize2019](https://prize.supplyframe.com) is Sponsored by: [![Supplyframe](img/79a7db035b8a2b6c2b7b0895c45b7de8.png)](https://supplyframe.com/)  [![Digi-Key](img/ba094a14c430ab81591a2abdc54a5363.png)](https://hackaday.io/digikey)  [![Microchip](img/5023ef0b7ff1aee311cba9b54a3ac9fe.png)](https://hackaday.io/microchip) 

 [https://www.youtube.com/embed/EHl2-ZyUp0o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/EHl2-ZyUp0o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

