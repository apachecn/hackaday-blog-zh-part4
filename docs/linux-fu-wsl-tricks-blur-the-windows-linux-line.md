# Linux Fu: WSL 诡计模糊了 Windows/Linux 界限

> 原文：<https://hackaday.com/2019/12/23/linux-fu-wsl-tricks-blur-the-windows-linux-line/>

我们不得不承认，我们对 WSL——Linux 的 Windows 子系统——有一种奇怪的迷恋。一方面，它为我们在 Windows 10 上运行我们喜爱的软件提供了更多选择。另一方面，我们想知道为什么我们不只是运行 Linux。有时候是因为我们很酷的笔记本电脑在 Linux 上不能很好地工作。其他时候，我们使用别人的电脑，我们不允许重新加载或双重启动。尽管如此，只要我们必须使用 Windows，我们很高兴有 WSL。[Hanselman]最近的一篇博客文章展示了一些非常酷的使用 WSL 的技巧，这些技巧让它变得更好。

## 探索 WSL

您知道可以使用 WSL 在 Windows 命令 shell 中运行 Linux 命令吗？例如，您有一个很长的目录，您想运行 grep:

```
dir c:\archive\* | wsl grep -i hackaday
```

当然，您可以从 bash 访问相同的目录:

```
ls /mnt/c/archive | grep -i hackaday
```

## 扩展ˌ扩张

[![](img/f0d159bc4912cbf2c42535e3ae0b5d03.png)](https://hackaday.com/wp-content/uploads/2019/11/pengwin.png) 许多技巧都依赖于 bash 不假定任何可执行文件扩展名这一事实。例如，如果您尝试从 bash shell 运行 explorer，什么都不会发生。但是如果您将。exe 扩展名，Windows 程序将运行，默认情况下，通常的 Windows 目录位于该路径中。

您确实需要注意路径名的转换。例如，如果您提供“.”作为 explorer 的一个参数，您将打开一个网络共享//wsl$/Ubuntu/home/user_name，例如。当然，那是另一个窍门。您可以使用该符号从 windows 访问 WSL 目录(显然，Ubuntu 和 user_name 可能会因您的安装而异)。然而，普通路径不起作用。

## 路径转换

但是，您可以使用 wslpath 实用工具双向转换路径:

```
$ wslpath
Usage:
-a force result to absolute path format
-u translate from a Windows path to a WSL path (default)
-w translate from a WSL path to a Windows path
-m translate from a WSL path to a Windows path, with '/' instead of '\'
```

例如:

```
$ explorer.exe `wslpath -w /bin`
```

## X11 及更多

[![](img/5295eea1f4ffb9f2cefeb3b105ff4657.png)](https://hackaday.com/wp-content/uploads/2017/03/vb.png)【Hanselman】讨论了许多技巧，包括一些关于使用开发工具和 git 的技巧。您还可以安装多种 WSL 风格，并将它们导出到其他 Windows 机器。他还提到使用付费工具 Pengwin 和 X410 运行 X11。我们说用[天鹅](https://hackaday.com/2017/03/29/swan-better-linux-on-windows/)就行了。

说到 Swan，它在任何 Windows 版本上都是 WSL 的绝佳替代品，而不仅仅是 Windows 10。事实上，它只是预配置了 X11 的 Cygwin，但这比试图让 X11 在一个裸的 Cygwin 安装上运行要容易得多。一方面，这是一个比 WSL 更桌面化的 Linux 解决方案。另一方面，WSL 加载真正的发行版，并与 Windows 10 很好地集成。但是如果你两者都装载，你也能得到两者的优点。

## 卖光？

如果可以选择，我们就用 Linux。老实说，如果你的工作流程主要是基于网络的，那就没什么关系了。你加载 Chrome 或者你选择的浏览器，一切正常。当然，我们的 Linux 机器往往比 Windows 更高效，运行也更好。

但是，如果你发现自己用的是 Windows，Cygwin 早就帮了大忙了。现在 WSL 是另一个让你的 Linux 工具在微软控制的机器上运行的工具。