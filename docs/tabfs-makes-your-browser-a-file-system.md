# TabFS 让你的浏览器成为一个文件系统

> 原文：<https://hackaday.com/2021/01/11/tabfs-makes-your-browser-a-file-system/>

像 Unix 一样，老式的 Linux 的理念是一切都应该看起来像一个文件。这种模式运行良好，操作系统的大多数核心特性都遵循这种模式。然而，许多现代的新增功能并没有真正地将事物视为文件，或者至少不是可以用其他工具轻松操作的文件。[Omar Rizwan]有一个方便的 Chrome 扩展，可以让你的浏览器标签看起来像你的文件系统的一部分。这不仅是一个新颖的想法，而且还出奇地方便。

这个扩展看起来有点像概念验证，所以安装有点粗糙，但它确实有效，它允许您做一些事情，否则您将不得不编写一个扩展或复杂的程序来进行屏幕抓取，这总是不太理想。

一旦有了包含所有选项卡的目录，就可以使用 ls、find 和普通的 glob 表达式等工具来搜索它们的标题、文本和 URL。还有一个基于文件的界面来控制每个标签。例如，如果你想关闭所有的 Hackaday 标签页(虽然，真的，你为什么要这样做？)您可以发出以下任何一个 shell 命令

```
rm ~/browser/tabs/by-title/*Hackaday*
echo remove | tee -a ~/browser/tabs/by-title/*Hackaday*/control

```

目前还不清楚你能向控制文件发送什么，但是源代码有一个到[扩展开发者文档](https://developer.chrome.com/extensions/tabs)的链接，看起来你可以使用其中的大部分方法(例如`goBack`、`reload`等)。).

你甚至可以从一个页面中抓取所有的图片，从 YouTube 音乐中提取当前的标题，以及许多其他的东西。每个扩展、每个窗口都有文件夹，选项卡按标题、ID 组织，或者您可以找到最后一个有焦点的选项卡。还有一种创建新标签页的方法。

默认情况下，程序安装在其选择的子目录中。我修改了代码以使用一个不同的目录，但是如果你这样做，不要在名字中加上~因为它不会像在 shell 中那样被展开。

当然，您可以在一个定制的扩展中做所有这些事情，但是对于简单的任务来说，这是一个相当大的负担。你也许可以用一些用户脚本扩展比如 GreaseMonkey 来完成其中的一些。但是将 shell 脚本和 Linux 工具的强大功能引入浏览器意味着您可以毫不费力地完成一些非常复杂的处理。

这个扩展确实会占用你很多浏览器，所以如果你有安全意识，你会想要仔细阅读[源代码](https://github.com/osnr/TabFS/issues)。现在要安装它，你必须自己编译，所以毫无疑问，你读到的代码和你的浏览器将要使用的代码是匹配的。我们期望有一天会有一个更容易的安装，像调试弹出窗口这样的东西有望最终消失。

你将如何处理目录中的标签？让我们知道你的想法。例如，我们想知道这对[测试](https://hackaday.com/2020/06/15/linux-fu-automation-for-chrome-and-the-desktop-by-matching-screenshots/)会有什么影响。TabFS 可能也会让[标签旋钮](https://hackaday.com/2019/04/30/a-physical-knob-for-browser-tabs/)成为一个更简单的项目。