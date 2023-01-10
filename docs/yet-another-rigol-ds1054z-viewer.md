# 另一款 Rigol DS1054Z 浏览器

> 原文：<https://hackaday.com/2021/05/26/yet-another-rigol-ds1054z-viewer/>

厌倦了眯着眼睛看示波器显示屏上的小数字，[Alfred]又名[Gaze@]决定自己动手，并且[编写了另一个工具](https://github.com/gaze-at/ds1054)来远程查看 Rigol DS1054Z 的图像。至少这是最初的想法。但是，它出乎意料地增长了——正如[阿尔弗雷德]所说，“项目越有趣，就越失控”。我们很了解这种感觉。

除了能够简单地查看和导出屏幕之外，该程序还实现了波形测量(我们不确定它是否使用了示波器的测量功能，或者实际上是在程序中执行测量)。正如你在 GitHub 库上运行的程序的动画 GIF 中所看到的，这些数字肯定是清晰易读的。他眯着眼看小屏幕的问题确实解决了。

这是用 Pascal(FPC·拉撒路)编写的，但是我们无法浏览这个程序，因为[阿尔弗雷德]还没有发布源代码。它只为 Linux 编写，他已经在 Ubuntu、Debian、Fedora 和 Manjaro 上进行了测试。该项目依赖于 Python、PyVisa 和 gtk2，并通过 USB 或 LAN 与您的 DS1054Z 对话。安装说明有很好的文档记录，但是正如[Alfred]自己警告的那样，如果您遇到由微妙的依赖版本冲突引起的麻烦，您可能需要成为一个书呆子和/或退休人员，有无限的时间来解决它们。根据[Alfred]的说法，既没有用户指南，也没有广泛的帮助。但是，在悬停文本中或通过按 F1 键可能会找到简单的提示。抛开免责声明不谈，这看起来是一个值得尝试的有趣项目。

正如[Alfred]所指出的，还有许多其他工具可以从您的 Rigol 示波器中获取数据和图像。[Jenny List]写了一个关于使用 Python 控制您的测试仪器的两部分系列文章[，这里有一个简单的 Python 脚本的例子](https://hackaday.com/2016/11/16/how-to-control-your-instruments-from-a-computer-its-easier-than-you-think/)[，它做了一个屏幕截图](https://hackaday.com/2019/03/30/grab-an-image-from-your-o-scope-the-easy-way/)。你有最喜欢的远程操作示波器的方法吗？请在下面的评论中告诉我们。