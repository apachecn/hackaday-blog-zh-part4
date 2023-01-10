# 应该是 20 世纪 70 年代的便携式串行终端

> 原文：<https://hackaday.com/2020/12/08/a-portable-serial-terminal-that-should-be-from-the-1970s/>

不起眼的独立串行终端可能早已从集体计算体验中消失，但以软件虚拟终端和串行转换器的幽灵形式，它仍然是计算机硬件黑客最基本的后备和必不可少的工具。[Mitsuru Yamada]已经创造了串行终端全盛时期应该制造的产品，[一个使用 6809 微处理器和老式惠普点阵 led 的独立手持终端](https://hackaday.io/project/176175-6802-serial-terminal)。在一个配有全按钮键盘的压铸盒子中，它完全可以卷到 DB-25 墙壁插座上，并登录到地下室的 PDP/11。

使用今天的器件，我们可能用一个单芯片微控制器和一个小型 LCD 或 OLED 面板实现同样的壮举，但用一个旧的微型计算机需要更多的系统建设。6809 是 20 世纪 70 年代的明智选择，因为它有一些板载 RAM，因此不需要 RAM 芯片。因此，整个过程只需要一个 2716 EPROM 用于软件，一个 6850 UART 和 MAX232 驱动器用于串行端口，以及一些 74 芯片用于粘合逻辑、芯片选择和 I/O 端口来处理键盘和显示器。箱子里没有电池，但毫无疑问，可以很容易地容纳。键盘本身也没有太多的信息，但在下面的视频中，我们看到了盒子打开时它的接线。

使用老式器件的终端的价值不仅在于*因为你可以*，还在于现代微控制器不容易拥有的东西。这些部件来自一个时代，当时计算机系统必须作为一系列外围设备组装在微处理器周围，因为它几乎没有板载设备，导致对计算机系统的理解更加深入。这并不是说 6809 在 2020 年是一个明智的选择，而是说它是一个*有趣的*选择。

相比之下，[这是一个使用当今技术的终端](https://hackaday.com/2017/04/06/hackaday-prize-entry-pocket-serial-terminal/)。

 [https://www.youtube.com/embed/JVC7F1cIqUo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/JVC7F1cIqUo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

