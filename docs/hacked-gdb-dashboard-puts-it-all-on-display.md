# 被黑的 GDB 仪表板展示了这一切

> 原文：<https://hackaday.com/2022/03/22/hacked-gdb-dashboard-puts-it-all-on-display/>

不是每个人都喜欢 GUI 界面。但是有些任务确实适合通过简单的命令行来完成。很少有人喜欢像 edlin 或 ed 这样的旧命令行文本编辑器。调试是另一项始终显示源文件和变量有意义的任务。当然，你不一定非要有 GUI *本身*。您也可以使用文本用户界面(TUI)。事实上，您可以用内置的 TUI 模式构建 gdb——GNU 调试器。尝试在 gdb 命令行中添加–tui，看看会发生什么。gdb 也有很多 GUI 前端，但是[cyrus-and]有一个简单的方法给[一个非常有用的类似 TUI 的接口](https://github.com/cyrus-and/gdb-dashboard)到 gdb，不需要重新构建 gdb，甚至不需要以任何方式侵入它的内部。

秘密？gdb 程序在启动时运行一个. gdbinit 文件。通过使用 Python 和一些 gdb 命令，[cyrus-and]使调试器为您的调试会话提供了一个漂亮的仪表板界面。如果你安装一个助手脚本，你甚至可以得到语法高亮。

系统使用模块，如果你愿意，你甚至可以添加你自己的定制模块和命令。您还可以控制每个仪表板显示屏上显示的模块。通常，仪表板会显示程序停止的时间。例如，在每个断点上。然而，gdb 有一个钩子系统，允许您在其他命令上使用适当命名的 dashboard 命令来触发 dashboard。使用仪表板命令的布局选项，您甚至可以在不同的时间触发不同的模块。

安装很简单。只要把。主目录中的 gdbinit 文件。如果你想突出语法，你也需要安装 Pygments。我们知道如果你愿意，你甚至可以在 Windows 下使用他的。

我们并不总是充分利用优势，但 gdb 是[实际上是惊人的](https://hackaday.com/2020/11/06/local-and-remote-debugging-with-gdb/)。[灵活的架构](https://hackaday.com/2020/06/04/adding-wifi-to-black-magic-for-wireless-gdb-action/)让各种有趣的事情成为可能。