# MicroOS 是不可变的 Linux

> 原文：<https://hackaday.com/2020/11/14/microos-is-immutable-linux/>

Linux 在非台式电脑中有很多用途。但是有一个问题。如果您的关键任务控制计算机或零售亭获得更新，然后出现故障，会发生什么情况？这在 Windows 上经常发生，在 Linux 上也可能发生。openSUSE 项目有一个答案: [MicroOS](https://microos.opensuse.org/) ，它宣称自己是不可变的。针对容器部署，操作系统承诺在运行时不改变磁盘的原子更新。如果更新破坏了某些东西，BTRFS 文件系统允许您回滚到以前的快照。【泰勒】[安装操作系统，并在下面的视频中演示](https://www.youtube.com/watch?v=Ve6ygUYobCw)。

正如[Tyler]发现的，默认安装的应用程序并不多。相反，您应该安装 flatpaks，这样应用程序就存在于它们自己的容器中，与操作系统和彼此隔离。

当然，这并不适合所有人。另一方面，拥有一台即使面对更新也非常可靠的计算机也是很诱人的。当然，您可以在任何支持 BTRFS 或 ZFS 的地方制作快照，但是除非您非常小心，否则您可能会遇到应用程序依赖性的问题，错误的更新仍然会毁了您的一天。该操作系统支持 GNOME 或 KDE，系统要求你可以在 1GB 的内存和 20GB 的磁盘空间中运行它。当然，如果你有更多，我们会想象你会更快乐。

如果您对 PI 的快照文件系统感兴趣，您可以在该平台上使用 [BTRFS](https://hackaday.com/2017/06/18/btrfs-for-the-pi/) 。我们想象你也可以使用[引信](https://hackaday.com/2013/11/06/writing-a-fuse-filesystem-in-python/)开发一些超级健壮的系统，如果有人还没有做过的话。

 [https://www.youtube.com/embed/Ve6ygUYobCw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Ve6ygUYobCw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

