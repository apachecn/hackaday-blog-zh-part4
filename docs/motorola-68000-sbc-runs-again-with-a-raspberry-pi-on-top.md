# 摩托罗拉 68000 SBC 再次运行，顶部有一个树莓 Pi

> 原文：<https://hackaday.com/2021/08/31/motorola-68000-sbc-runs-again-with-a-raspberry-pi-on-top/>

单板计算机已经存在很长时间了:今天你可能在使用 Raspberry Pi、Arduino 或 ESP32，但三十年前你可能会发现自己在为 KIM-1、Intel SDK-85 或摩托罗拉 68000 教育计算机板编程。这种主板通常是由处理器制造商制造的，用来展示他们的最新芯片，并培训可能在设计中使用这些芯片的工程师。

[Adam Podstawczyński]发现自己试图操作一辆 1981 年的摩托罗拉 ECB。该板包含一个 68000 CPU(用于几个 Macintoshes 和 Amigas)、32kb RAM 和一个名为 TUTOR 的 ROM 程序。由于没有任何键盘或显示器连接，与该系统通信的唯一方式是一对串行端口。[Adam]决定通过添加一个带有 RS232 帽子的 Raspberry Pi 扩展来提高电路板的易用性。该附加板带有两个串行端口，支持旧设备中使用的+/- 12 V 信号电平。

建立一个可靠的连接需要几个小时的实验、调试和阅读大量的 ECB 文档；事实证明，串行端口可以根据握手线的状态以不同的模式工作。当 Pi 的串行端口最终设置为正确的模式时，旧计算机开始响应终端窗口中输入的命令。用于在磁带上录制节目的音频接口被证明更加难以可靠地运行，可能是由于电容器的退化。这不是一个大问题，因为欧洲央行的第二个串行端口也可以用来直接将程序保存和加载到其内存中。

随着串行连接的工作，[亚当]然后转向他的设置美学，并决定用激光切割丙烯酸和金属垫片制作一个简单的外壳。用于串行端口的定制带状电缆和用于电源连接的 ATX 分线板完成了该项目，这台有 40 年历史的教育计算机现在准备向它的新主人传授 68000 编程的所有细节。在视频中(插播在广告之后),他展示了让欧洲央行运转起来的整个过程。

[Adam]之前用[一台 Commodore 64 和一台 Arduino](https://hackaday.com/2017/01/14/c64-keyboard-emulation-over-serial/)做了一个类似的巧妙设置。[杰夫·特兰特]从头开始重新创建了一个类似的 [68000 开发板](https://hackaday.com/2017/02/27/an-old-68000-sbc-is-new-again/)。几年前，我们甚至推出了自己的[定制 68k 电脑](https://hackaday.com/2014/02/20/hackaday-68k-a-new-hackaday-project/)。

 [https://www.youtube.com/embed/oiJ9J2WyPWY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/oiJ9J2WyPWY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

