# 6502 上的虚拟现实

> 原文：<https://hackaday.com/2019/06/23/vr-on-the-6502/>

MOS 技术 6502 是 20 世纪 80 年代比较流行的处理器之一。它运行的是 Commodore 64、改良版的 NES 以及一大堆其他硬件。按照现代标准，它勉强适合运行计算器，但没关系——[[Nick Bild]构建了一个运行在复古 CPU 上的 VR 游戏！](https://www.hackster.io/nickbild/vectron-vr-a98a0e)

[Nick]的项目建立在他的 6502 计算机上，即 Vectron 64。作为一个试验板构建，很容易修改东西和添加额外的硬件，这正是他所做的。VR 系统使用两个 320 x 240 的 LCD 屏幕，每只眼睛一个。这些都是通过 SPI 控制的，但不起眼的 6502 根本没有速度来为视频游戏提供足够快的时钟输出。相反，增加额外的硬件来产生脉冲以运行屏幕。还有一堆其他巧妙的技巧帮助游戏变得可玩，比如将 CPU 超频到 1.75 MHz，同时在两个屏幕上绘制共同的元素。

为了测试虚拟现实系统，[尼克]编写了一个基本的小行星虚拟现实游戏。在没有硬件的情况下演示这个游戏并不实际，但是我们很想尝试一下。8 位图形的低分辨率 VR 游戏有一些引人注目的东西，我们希望看到这个概念在未来得到进一步发展。

更多的咕噜声将使这个项目更有能力，为此，[一个运行在 20MHz 的 6502 可以派上用场](https://hackaday.com/2018/12/15/this-6502-made-from-74-series-logic-can-run-at-20-mhz/)。休息后的视频。

【感谢 Fred Gimble 的提示！]

 [https://www.youtube.com/embed/pnfFcg1cZ8U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/pnfFcg1cZ8U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

