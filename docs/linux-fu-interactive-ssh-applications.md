# Linux Fu:交互式 SSH 应用程序

> 原文：<https://hackaday.com/2019/09/06/linux-fu-interactive-ssh-applications/>

[Drew de fault]最近写了一些有趣的说明，关于如何[打包交互式的基于文本的 Linux 命令](https://drewdevault.com/2019/09/02/Interactive-SSH-programs.html)供用户通过 ssh 访问。乍一看，这似乎很简单，但是其中有很多细微的差别，而且[Drew]在这方面做得很好。

一种简单的方法——但不是非常通用的——是创建一个用户，并让您想要运行的程序使用默认 shell。使用的示例是让/usr/bin/nethack 成为 shell，现在人们可以作为该用户登录并玩 nethack。简单吧？然而，有更好的方法到达那里。

有几个问题。首先，如果用户向 nethack 这样的程序传递命令行，事情就会变得混乱。但是，您可以向。ssh/authorized_keys 文件，用于选择登录时使用真实 shell 运行的命令。您可以将 shell 设置为像/bin/sh 或 rbash (restricted bash)这样简单的东西，并使用它来启动 nethack 或您选择的二进制文件。受限制的 shell 阻止用户执行诸如更改目录、设置某些环境变量等操作。它针对恶意活动提供了一定程度的安全性，尽管可能不是严重的恶意活动。

为了完善这个例子，[Drew]展示了他如何将这些想法应用到一个真实的工作系统中。他有一系列 Python 脚本，这些脚本与 [Sourcehut](https://drewdevault.com/2019/08/19/Introducing-shell-access-for-builds.html) 持续集成构建一起工作。

我们喜欢小的 ssh 工具。虽然我们喜欢 ssh，但如果你的连接不可靠，你可能更喜欢 [Mosh](https://hackaday.com/2016/11/01/ssh-enters-the-mosh-pit/) 。