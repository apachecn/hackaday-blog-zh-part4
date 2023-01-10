# Linux 傅:拉皮条你的管道

> 原文：<https://hackaday.com/2018/11/07/linux-fu-pimp-your-pipes/>

使用 Linux(或类似的 OS)命令行的最大好处之一就是使用管道。简单地说，管道接受一个命令的输出，并将其发送到另一个命令的输入。您可以使用管道做很多事情，但是有时很难为一组管道确定正确的顺序。一个常见的技巧是逐步攻击它。也就是说，执行一个命令，并使用正确的选项和输入让它工作。然后添加另一个命令，直到成功为止。不断添加命令和调整，直到您获得最终结果。

这很好，但[akavel]想要更好，并使用 Go 创建了[“up”——一个管道](https://github.com/akavel/up)的交互式查看器。

## 管道哲学

管道可以做很多事情。它们符合最初的 Unix 哲学，即让每个工具真正做好一件事。Pipe 在允许 Linux 命令相互对话方面做得非常好。如果你想了解所有关于管道的知识，看看 Linux Info 项目的指南。他们甚至谈论为什么 MSDOS 管道根本不是真正的管道。(write up 没有提到的一件事是命名管道。如果你现在想了解更多，可以做一个“man fifo ”,也许这将是未来 Linux Fu 的主题。)

这个名为 *up* 的程序在您对管道进行更改时持续运行并重新运行您的管道。这样，您所做的每一个更改都会立即反映在输出中。这是视频，这是一个展示 *up* 互动本质的快速视频。

 [https://www.youtube.com/embed/Sh2uCM7iXps?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=23&wmode=transparent](https://www.youtube.com/embed/Sh2uCM7iXps?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=23&wmode=transparent)



## 安装

GitHub 页面假设你知道如何安装 go 程序。我试图做一个构建，但我没有几个依赖。事实证明，最简单的方法是运行下面这行代码:

```
go get -u github.com/akavel/up
```

这会将可执行文件放在~/go/bin 中——这不在我的路径上。当然，您可以将其复制或链接到您的路径上的某个目录，或者将该目录添加到您的路径中。例如，您也可以设置一个别名。或者像我在视频里做的那样，每次都指定。

## 完美？

这似乎是一个整洁简单的工具。还有比这更好的吗？嗯，我有点难过，你不能在管道上使用 emacs 或 vi 编辑键，至少据我所知不能。这正是那种你想要退回到中间并改变一些东西的事情。不过，你可以使用箭头键，所以这很了不起。我也希望可滚动窗口有一个搜索功能。

不过，除此之外，这个小工具也没什么不喜欢的。如果说写管道就像用 C 编译器，那么 up 更像是写一个交互式的 Basic 程序。