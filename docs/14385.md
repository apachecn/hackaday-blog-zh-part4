# GameTank 是最新最棒的 8 位游戏主机

> 原文：<https://hackaday.com/2022/08/02/the-gametank-is-the-latest-and-greatest-8-bit-game-console/>

NES、Atari 2600、Apple II、Commodore 64 和 TurboGrafx-16 只是围绕 6502 CPU 构建的众多游戏控制台和家用电脑中的一部分。虽然 6502 自 90 年代中期以来已经相当过时，但这并没有阻止黑客在 21 世纪用它来构建新系统。今天我们甚至可以向你展示一个全新的基于 6502 的游戏主机:[游戏坦克，由【克莱德·谢弗】设计和建造。](https://clydeshaffer.com/gametank/)

游戏坦克被设计成任何人都可以很容易地建造，因此大部分是由 DIP 芯片建造的，这些芯片可以在任何组件经销商处买到。主 CPU 是一个运行频率为 3.5 MHz 的 WD65C02，由一个 6522 I/O 控制器和 32kb RAM 辅助。复合视频是由分立逻辑芯片构成的巧妙电路产生的。视频卡配有用于快速传输的 DMA，甚至包括一个阻击器，这使它能够在不加载 CPU 的情况下在屏幕上快速移动图像。

对于控制器，[Clyde]决定采用或多或少符合行业标准的 DE-9 连接器游戏手柄，就像 Sega Genesis 和各种 Atari 游戏机上使用的那样。他还制作了自己的控制器，一个 3D 打印的控制器，有四个方向按钮，三个动作按钮和一个启动按钮。这些按钮是用 Cherry MX Clear 开关实现的——对于游戏手柄来说，这可能是一个不寻常的选择，但它们显然非常适合长时间的游戏。

游戏机本身也装在一个印刷外壳中，其设计让人想起任天堂 64。游戏卡带插在顶部，包含一个 EEPROM 芯片，可以用特殊的编程器写入。盒式磁带端口还可以输出几个内部信号，因此可以用作扩展端口，类似于超级 NES 盒式磁带可以容纳增强芯片的方式。

目前可用的游戏包括*俄罗斯方块*、办公室主题平台游戏*格子骑士*、名为*被诅咒的恶魔*的*塞尔达*风格冒险，以及翻拍的经典病毒动画*坏苹果*。[Clyde]提供了一个全面的工具和示例代码堆栈，并邀请任何感兴趣的人帮助为该平台开发更多的软件。还有一个硬件精确仿真器，它不仅在你为系统编写新代码时有用，而且在你仅仅想在你的浏览器中尝试现有游戏时也有用。

滚动你自己的 6502 系统是非常有趣的，这些年来我们已经看到了几个例子:一些是用大量电线构建的[，一些是带有聪明编程语言](https://hackaday.com/2019/04/04/a-6502-computer-with-acres-of-breadboard-and-dozens-of-chips/)的[，一些是小到可以戴在手腕上的](https://hackaday.com/2018/02/13/a-6502-with-a-custom-langauge/)，还有一些只是制作精美的。

 [https://www.youtube.com/embed/JOmsZlUlqlE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/JOmsZlUlqlE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

