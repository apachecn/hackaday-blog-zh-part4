# 用 Lisp 编程这个徽章

> 原文：<https://hackaday.com/2019/01/10/program-this-badge-in-lisp/>

这个[硬件徽章是用 Lisp](http://www.technoblogy.com/show?2AEE) 编程的电脑。只要你懂 Lisp，你就可以使用内置键盘在徽章上编写自己的程序。

如果有一件事我们真的很想看到，那就是人们基于他人的灵感推进自己的项目。[戴维·约翰逊-戴维斯]的 Lisp 徽章就是一个完美的例子。这个版本的界面灵感来自[Voja Antonic]为 [2018 年贝尔格莱德大会徽章](https://hackaday.com/2018/05/15/retro-computer-badge-for-hackaday-belgrade-has-everything-you-wished-for-back-in-the-day/)设计的硬件设计，是早期单板 Lisp 机器的升级版，现在配备了集成键盘。

与用 BASIC 编程的贝尔格莱德徽章不同，这个新徽章是用 [uLisp 编程的，uLisp 是为微控制器设计的通用 lisp](http://www.ulisp.com/show?3L) 的子集。面对现实吧，BASIC 是复古的，Lisp 更是如此，只不过被 FORTRAN 提前为最古老的高级语言。因此，如果您喜欢在小型设备上进行复古式编程(实际上很小)，您应该考虑构建一个这样的设备。

[![](img/0d5a374f9f39c64c7d43e0efcdeee5a1.png)](https://hackaday.com/wp-content/uploads/2019/01/lispbadgeback.jpg) 一个 16 MHz 的 ATmega 1284P 作为徽章的大脑，允许存储 2816 个 Lisp 细胞，而 256×64 像素的有机发光二极管显示器以 16 种灰度显示 8 行 42 个字符。完整的 I/O 连接包括 4 路模拟输入、2 路模拟输出、I2C、SPI、串行和一些 GPIOs，可与任何东西接口。电源来自 LiPO 电池，标称电压为 3.7 V，不太符合数据手册中以 16 MHz 运行处理器的要求，尽管它在实践中似乎工作良好。真正谨慎的建设者可以选择 12 兆赫晶体移植，以避免任何问题的可能性。

键盘布局针对 uLisp 编程进行了优化:删除了不必要的键，最重要的括号在底部一行有自己的专用键。这大概是为了方便使用，但我们怀疑这也将使括号键开关更容易更换，当它们不可避免地因过度使用而磨损时[强制性 Lisp/括号笑话]。

至于输入 uLisp 程序，你可以简单地使用键盘。内置编辑器缓冲了全屏文本，并包括括号匹配，在您键入时突出显示每一对。我们猜测在不久的将来我们不会看到 Emacs 的实现，所以这个括号管理对于一个基于徽章的编辑器来说是一个很好的特性。如果你发现键盘很难输入，你也可以通过串口输入程序。

我们真正想看到的另一件事是开源项目。[大卫]在这一点上也没有让我们失望。PCB 的 Eagle 设计文件以及徽章的源代码可在 GitHub 上获得[。PCB 也在奥什公园](https://github.com/technoblogy/lisp-badge/tree/master/Eagle%20files)上[共享，里面有安装 bootloader 和上传代码的详细说明。](https://oshpark.com/shared_projects/wnj60xEU)

如果你喜欢可编程徽章，也可以看看贝尔格莱德设计的继任者[2018 Hackaday super co 徽章](https://hackaday.io/project/161859-2018-hackaday-superconference-badge)。

感谢[斯文]的提示！