# Z80 板，零件非常少

> 原文：<https://hackaday.com/2020/07/17/a-z80-board-with-very-few-parts/>

Z80 是那种既容易买到又容易使用的旧 CPU 之一——至少在某些版本中是这样。[博士伏特]把可能是最简单的设置放在一起，以获得一个工作的 Z80 系统。当然，他有处理器。但其他一切——时钟、内存和电源——都来自 Arduino Mega 2560。你可能会说那是两个芯片，但实际上电路板上有几个芯片。另一方面，你也许可以用一台光秃秃的 ATMega 2560 来完成同样的特技。

我们以前见过这种情况，但通常需要更多的支持芯片。如果你是一个纯粹主义者，Volt 博士]也有一些 [Z80 和 CP/M 实验](https://www.hackster.io/michalin70/cp-m-on-a-minimal-z80-computer-cecaf7)，其中 Arduino 只充当计算机的磁盘驱动器，只有两个支持芯片。你可以在下面看到这两个项目的三个视频。

然而，我们被第一个项目的简单所震惊。只需要大约 100 行源代码，其中一些是注释。Arduino 甚至提供系统内存(1K ),您可以通过更改 memory.h 文件并重新加载 Arduino 来初始化它。

代码为中断和时钟做了一点设置，然后就开始旋转。Arduino 在 CPU 读取时获得中断，在 CPU 写入时获得不同的中断。所有的内存读取都从模拟的 1K RAM 中提取，内存写入也是如此。写入代码还可以检测 I/O 端口写入，并将数据发送到 Arduino 串行端口。您写入哪个 I/O 端口似乎并不重要。

这让我们想起了我们最喜欢的[廉价 Z80 项目](https://hackaday.com/2017/01/02/retrocomputing-for-4-with-a-z80/)。该板以类似的方式使用 ATMega32A，但也有外部 RAM。如果你添加几个 EEPROMs 作为磁盘驱动器，它就位于两台计算机的中间。用这么少的零件，很容易在[相当小的空间](https://hackaday.com/2019/09/17/a-curiously-strong-z80-in-your-pocket/)得到这些 8 位的奇迹。

 [https://www.youtube.com/embed/pNjEzovSfrY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/pNjEzovSfrY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/yR566HNj0ao?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/yR566HNj0ao?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/tocXaInkarE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=8&wmode=transparent](https://www.youtube.com/embed/tocXaInkarE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=8&wmode=transparent)

