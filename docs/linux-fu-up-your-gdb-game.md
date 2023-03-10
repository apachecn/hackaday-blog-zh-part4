# Linux 傅:收起你的游戏！

> 原文：<https://hackaday.com/2022/06/14/linux-fu-up-your-gdb-game/>

如果你想买车，有很多选择。如果想买喷气式飞机，选择就少了。如果你想使用大型强子对撞机，你有一个选择。越难创造的东西，越不可能有很多。如果你正在寻找一个 Linux 调试器，只有几个选择，但是 gdb 肯定是你最常找到的。有 lldb 和一些非开放的商业产品，但是大多数情况下，您将使用 gdb 在 Linux 上调试软件。

当然，并不是每个人都喜欢 gdb 基于文本的界面，所以它不缺少前端。事实上，gdb 有两个潜在的内置接口，尽管取决于你如何安装 gdb，你可能不会同时拥有它们。当然，如果你使用 IDE，它很可能是 gdb 的前端。但是核心是 gdb，并且——通常——在某个地方有一个窗口，你可以把 gdb 命令塞进去。甚至 emacs——可能被认为是最初的 IDE——也可以运行 gdb，并给你一种 GUI 体验。

## 不需要前端

曾经有一段时间，洞察力很流行。这不是广发银行的前端。它是 gdb 的实际副本，内置了 Tk/Tcl GUI。然而，由于包装问题，它不再受欢迎了，这是我的老朋友杰夫·邓特曼[在每个人都放弃它的时候详细谈到的。](https://www.contrapositivediary.com/?p=1396)

然而，仍然有一种方法可以在没有前端的情况下更好地使用 gdb。-tui 标志。这给你的不是一个图形用户界面，而是一个文本用户界面，如下图所示。

![](img/db3f800fc2d0277dbc167e5a50db7b44.png)

The gdb TUI mode lets you see more data at one time but still leaves something to be desired

虽然我并不总是一个图形用户界面的粉丝，但调试是一个让大量信息同时出现在屏幕上很有意义的地方，所以这是一个我会经常尝试使用比简单的命令行稍微好一点的东西的地方。默认视图只显示您的源代码和命令窗口，但是您也可以打开寄存器显示，启用反汇编显示，以及更改所有内容的布局。尝试命令“布局分割”或“布局规则”来查看一些不同的显示。“布局 src”命令将把事情恢复到开始时的样子。如果你想认真使用 TUI 模式，[查看文档](https://sourceware.org/gdb/onlinedocs/gdb/TUI-Commands.html)。值得注意的是，您可以随时使用“tui enable”打开该模式，使用“tui disable”关闭该模式并返回普通 gdb。

## 为什么不是 Web？

如今，一切都可以在网络浏览器中运行，为什么不能在调试器中运行呢？gdbgui 前端就是这样做的。当然，调试器不在浏览器中运行，只在连接到本地服务器的用户界面中运行。您可以在附图中看到使用 gdb-multiarch 针对 ARM 可执行文件运行的程序。

![](img/734da75369477ffa7fb2b1e672fbe7ce.png)

The gdbgui interface runs in a browser

所有的前端，当然，寻找正常的 gdb 可执行文件。但是如果你正在远程调试像 AVR 或 ARM 芯片这样的东西，你需要找到指向正确的 gdb 程序的方法。对于 gdbgui，这是命令行上的-g 选项。不清楚是否有办法使用扩展远程协议连接到服务器(这里是 OpenOCD)。至少在默认情况下，它使用的是标准的远程协议，这种协议功能较差。

另一个在浏览器中运行界面的类似选择是 [gdbfrontend](https://github.com/rohanrhu/gdb-frontend) 。它还需要一个-g 或–gdb-executable 选项来设置底层 gdb 程序的不同选择。你可以在下面看到它的样子。

![](img/9eaff7f4b46453495fedd8785ef49576.png)

The gdbfrontend program has many colorful (and sometimes distracting) themes

和 gdbgui 一样，似乎也没有办法配置前端使用扩展远程协议，这就造成了用 OpenOCD 调试时的一些限制。一个有趣的功能是协作按钮，它可以让你在屏幕上绘图，大概是在与他人共享屏幕或为教室投影屏幕时。

## 其他选择

另一个好看的选项是 [Seer](https://github.com/epasveer/seer) ，它不在浏览器中运行。注意，不幸的是，这与 Ubuntu 中的 seer 包不同。对于 seer，您必须退出弹出的第一个对话框，然后转到设置来更改 gdb 可执行文件。然而，我在 GUI 中设置断点时遇到了问题。如果你使用 gdb 终端的话，断点看起来确实可以工作，但是这有点违背了初衷。如果你能让它工作的话，它看起来确实有一个有趣的“数组可视化工具”。我满足于一个 seer 调试一个非常简单的 Linux 程序的镜头，它做得很好。

[![](img/32561cfb64c16c82ef5f6b04f285f5db.png)](https://hackaday.com/wp-content/uploads/2022/06/seer.png)

Seer debugging a Linux executable

我怀疑所有这些程序在普通的 Linux ELF 文件上使用普通的 gdb 都能很好地工作。毫无疑问，所有的问题都是因为我使用 OpenOCD 作为 gdbserver，并与一个远程 ARM 芯片进行对话，这可能不是开发人员经常测试的事情。尽管如此，这两个基于浏览器的工具还是能够完成任务，尽管它们忽略了扩展协议的特性。

你在乎吗？如果你用的是集成了 gdb 的 IDE，也许不是。或者你太强硬了，根本不会使用调试器。那很好。但是在你需要 gdb 的时候，这些前端可以让你更有效率，让你更专注于真正重要的事情:找到 bug。

老实说，如果你正在考虑使用 TUI 界面，看看我们今年早些时候谈到的仪表板。如果你还没有接触过 gdb 远程调试，玛雅·波许[已经帮你搞定了](https://hackaday.com/2020/11/06/local-and-remote-debugging-with-gdb/)。