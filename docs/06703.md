# Linux-Fu:平行宇宙

> 原文：<https://hackaday.com/2020/06/29/linux-fu-parallel-universe/>

在某种程度上，您只是耗尽了处理能力。不可否认，那个点越来越远，但你仍然可以到达那里。如果您用完了 CPU 时间，答案可能是添加更多的 CPU。然而，有时还有其他瓶颈，如内存或磁盘空间。但是，也有可能您可以访问多台计算机。谁在自己的社交网络中没有几个红莓呢？或者是地下室的服务器？或者甚至是“云中”的一些远程服务器 GNU Parallel 是一个工具，它可以让你将工作分散到多个任务上，既可以是本地的，也可以是远程的。在某些方面，它很简单，因为它看起来有点像`xargs`,但是是并行执行的。另一方面，它有无数的选项和配置，可能会让它使用起来有点令人生畏。

## 关于 xargs

如果你不使用`xargs`，这是一个非常简单的程序，它可以让你对文件列表做一些事情。例如，假设我们想使用 grep 在所有 C 源文件中搜索字符串“hackaday”。你可以写:

找到。-姓名' *。xargs grep -i hackaday

这里，`xargs`抓取一个输入行，调用`grep`，在`grep`完成后，它重复这个过程，直到用完所有的输入行。(注意:处理带有空格的文件有点棘手。使用-d '\n '可能会有帮助，尽管不是所有版本的 xarg 都支持它。)

在最简单的情况下，Parallel 做同样的事情，但是它可以一次多次执行`grep`——或者您正在使用的任何东西。在本地机器上，这允许您使用多个 CPU 来改进计时。然而，您也可以将工作分散到拥有无密码`ssh`登录的不同机器上。

## 民众

GNU Parallel 的作者有一个系统的多部分视频演示。你可以在下面看到第一部分。[教程](https://www.gnu.org/software/parallel/parallel_tutorial.html)也非常好，它澄清了一些在线手册中可能不明显的细节。

只是为了自娱自乐，我取了一个目录，其中有一些大的`mp4`文件，并使用`xargs`和`parallel`来`gzip`每个文件。我知道，我知道。文件已经被压缩，所以`gzip`不会做太多。但我只是想要一些大任务的时间。结果如下:

```
[:~/Videos/movies] $ time find *.mp4 | xargs -d '\n' gzip

real    6m10.796s
user    2m52.828s
sys     0m9.718s
[:~/Videos/movies] $ time find *.mp4 | parallel --jobs 8  -d '\n' gzip

real    5m25.050s
user    2m56.676s
sys     0m7.732s
```

不可否认，这不太科学，节省大约 45 秒并不是一个巨大的收获，但仍然。我选择了八个任务，因为我有一个八核处理器。您可以根据当时正在做的其他事情来改变设置。

 [https://www.youtube.com/embed/OpaiGYxkSuQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/OpaiGYxkSuQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



## 遥远的

如果您想要使用远程计算机处理数据，您需要无密码`ssh`远程访问另一台计算机(或多台计算机)。当然，远程计算机可能没有相同的文件和资源，所以默认情况下，您的命令只在远程服务器上运行是有意义的。您可以提供一个逗号分隔的服务器列表，如果您使用“:”(只是一个冒号)的服务器名称，您将在处理作业时包括您的本地机器。

如果你有一台动力不足的电脑需要帮助，这可能会非常有用。例如，我们可以想象一台基于 Raspberry Pi 的 3D 打印机要求一台远程主机并行切割一堆模型。即使您认为您没有任何计算负担，Parallel 也可以做一些事情，比如处理来自`tar`归档的文件，因为它们是解压缩的，不需要等待其余的文件。它可以将`grep`的工作分配给你的 CPU 或内核。

老实说，详细解释每个特性需要很多时间，但是我希望这能鼓励你阅读更多关于 GNU Parallel 的内容。在视频和教程之间，您应该对使用这个强大的工具可以做的一些事情有了很好的了解。