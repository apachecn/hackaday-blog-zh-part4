# 跟踪二进制变化:学习 ELF 的不同方式

> 原文：<https://hackaday.com/2019/04/07/tracking-binary-changes-learn-the-diff-erent-ways-of-the-elf/>

当开始一个新项目时，源代码控制通常是第一步(或者应该是，我们希望如此！).将变更分解成更小的块并管理它们之间的变更，使得开发人员之间更容易共享工作，并在错误发生后捕捉和恢复错误。随着项目复杂性的增加，人们通常希望在它的基础上增加一些其他的特性，比如自动构建、测试和部署。

这些对于固件来说不太常见，但是自动构建(“持续集成”或 CI)非常容易设置，并且可以立即让您看到一系列潜在的问题。忘记签入新标题？源不会构建。调整了链接器脚本并破坏了一些东西？软件不会构建。重命名了一个变量却忘了几个引用？软件不会构建。但是仅仅构建软件只是一个开始。[noseglasses]组装了一个名为 [elf_diff 的工具，使跟踪二进制更改](https://github.com/CapeLeidokos/elf_diff)变得更容易，这是对任何构建管道的一个极好的补充。

在固件世界里，闪存空间是有限的，最好能控制代码的大小。这可以通过多种方式实现。人工检查。地图文件(俗称“地图文件”)是最容易开始的地方，但不利于随着时间的推移自动跟踪。映射文件由链接器生成，并跟踪编译期间生成的目标文件的编译大小，以及最终输出文件的闪存和 RAM 布局。[这里有一个例子](https://github.com/borgel/sympetrum-v3/blob/master/Firmware/Releases/v5/sympetrum-v3.map)由 GCC 从一个小电子徽章生成。这是一个相对简单的单一用途设备，该文件已经有大约 4000 行长。想知道一个函数占用了多少代码空间吗？就在那里，但是你需要去挖掘它。

elf_diff 通过将该过程包装在一个方便的报告中来实现自动化，该报告可以作为 CI 管道的一部分自动生成。基本上，该工具将一个旧的和一个新的 [ELF 文件](https://en.wikipedia.org/wiki/Executable_and_Linkable_Format)作为输入，并生成 HTML 或 PDF 报告[，就像这个](https://github.com/keyboardio/Kaleidoscope/files/3008128/kaleidoscope_change_report_dynamic_LED_modes.pdf)一样，其中包括像这里显示的图像这样的读数。结果表突出显示了几类二进制更改。最突出的是代码和 RAM 部分的大小变化，但它也将代码大小变化分解为单个符号(想想结构和函数)。[noseglasses]有一个[配套脚本](https://github.com/CapeLeidokos/Leidokos-ChangeReport)，通过编译一对固件文件并运行 elf_diff 生成报告来简化 CI 过程。对于您自己的构建系统集成，这可能是一个有用的起点。

感谢[obra]的提示！有没有将现代软件实践应用于固件开发的技巧和诀窍？在评论里告诉我们吧！