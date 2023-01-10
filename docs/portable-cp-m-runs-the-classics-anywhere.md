# 便携式 CP/M 在任何地方都能运行经典

> 原文：<https://hackaday.com/2020/07/23/portable-cp-m-runs-the-classics-anywhere/>

如果你想运行一个老的 CP/M 程序——也许你想运行 WordStar 或者播放 StarTrek——你有几个选择。一是收购一些经典硬件。您还可以使用 Z80 或模拟 Z80 的其他处理器来构建新的计算机。最后，您可以在当前计算机上模拟旧硬件。来自[ivanizag]的 iz-cpm 项目采用了最后一种方法。与一些模拟器不同，iz-cpm 并不试图在一个模拟环境中模拟一切。相反，它直接访问您的文件系统，因此它允许 CP/M 可执行文件更多地运行，就像它们是一个本地程序一样。

你可以把它当成 CP/M 的 Wine，代码可以移植到 Linux，Windows，或者 MacOS。尽管作者提到它不能在 CP/M 上运行！该计划可以运行一个可执行的独立，这意味着你可以设置。COM 文件自动执行，如果你想。

该机器看起来像一个 Kaypro，并模仿 ADM-3A。有一个脚本可以下载有趣的 CP/M 软件，例如 WordStar、Basic 和 Zork。如果你想调试的话，你可以跟踪调用甚至 CPU 指令。不过，说到调试，您可能真的需要这么做。

在试用这个程序时，我们注意到 WordStar 有一些奇怪的行为。将文件保存到驱动器 A 是可行的，但是如果你保存到其他地方，文件最终会保存到驱动器 A。这使 WordStar 感到困惑，因为它试图从另一个磁盘上重新读取文件，因此它删除了您正在处理的文本。我们在 GitHub 上报告了这个问题，几个小时后作者就修复了它。你必须热爱开源社区。

这个程序是用 Rust 编写的，最近似乎越来越流行。该计划是一个进入 CP/M 黑客的好方法，尤其是如果你对 Rust 编程感兴趣的话。

如果你想要真正的硬件，这款 [Z80 电脑](https://hackaday.com/2017/01/02/retrocomputing-for-4-with-a-z80/)的价格很难被击败。然而，拿起 [PCB](https://hackaday.com/2018/07/28/the-4-z80-single-board-computer-evolved/) 并检查我们的[对它的更新](https://github.com/wd5gnr/Z80-MBC)。