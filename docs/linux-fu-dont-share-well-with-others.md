# Linux 傅:不好好和别人分享

> 原文：<https://hackaday.com/2021/12/28/linux-fu-dont-share-well-with-others/>

在幼儿园，你学会了应该分享。但是对于计算机安全来说，共享往往是一件坏事。从版本 2.6.24 开始，Linux 内核引入了名称空间的概念。那是几年前的事了，但是名称空间并没有被很多人使用，尽管有工具可以操纵它们。当然，您并不总是需要名称空间，但是当您确实需要它时，它的功能是无价的。简而言之，名称空间允许您为进程提供它自己的私有资源，更重要的是，防止进程看到其他名称空间中的资源。

原来，您一直在使用名称空间，因为您运行的每个进程都存在于某个名称空间集合中。我说 set，是因为不同的资源有许多名称空间。例如，您可以设置一个不同的网络名称空间，为一个进程提供它自己的一组网络项目，包括路由表、防火墙规则和所有其他与网络相关的内容。

所以我们来看看 Linux 是怎么不共享名字的。

可能的命名空间有:

*   挂载—文件系统挂载。可以与其他名称空间共享挂载，但是必须显式地这样做。
*   UTS——这个名称空间控制诸如主机名和域名之类的东西。
*   IPC——具有独立 IPC 名称空间的程序将拥有自己的消息队列、信号量、共享内存和其他进程间通信项目。
*   网络——命名空间中的进程将拥有自己的网络堆栈和相关配置。
*   PID——PID 名称空间中的进程看不到名称空间之外的其他进程。
*   Cgroup—一个命名空间，为 CPU 管理提供 cgroup 装载的虚拟化视图。
*   用户–个人用户、组等。

显然，其中一些比其他的更有用。然而，很容易看出，如果你有一个协作程序系统，你可能会发现为 IPC 或它们之间的网络创建一个私人空间是有吸引力的。

## 完蛋

如果想在 shell 中试验名称空间，可以使用`unshare`。这个名字可能看起来很奇怪，但是这个命令的名字来源于这样一个事实:一个新的进程通常共享其父进程的名称空间。`unshare`命令允许您创建新的名称空间。

`unshare`的一个关键特性或怪癖是，默认情况下，它用创建的新名称空间运行一个程序，但是它不将该程序与这些名称空间相关联。相反，新的命名空间会被程序创建的任何子对象所使用。您可以添加一个–fork 选项，让它更好地工作。

例如，让我们在自己的私有爱达荷州开始一个新的 shell:

```

sudo unshare --pid --fork --mount-proc /bin/bash
ps alx

```

如果您在没有单独名称空间的情况下尝试该命令，您将得到一个很长的进程列表。但是我们的新名称空间中的输出要小得多:

```

F   UID     PID    PPID PRI  NI    VSZ   RSS WCHAN  STAT TTY        TIME COMMAND 
4     0       1       0  20   0  10820  4376 -      S    pts/6      0:00 /bin/bash 
0     0       9       1  20   0  12048  1168 -      R+   pts/6      0:00 ps alx

```

你必须考虑一下不同的工具是如何工作的。例如，`ps`从`/proc`中读取数据，所以如果我们不提供 `--mount-proc`，它仍然会显示所有的主进程。(试试吧。)你将无法与他们互动，但因为你可以阅读`/proc`，你仍然可以看到他们。`--mount-proc`标志实际上只是`--mount`(获得一个新的挂载名称空间)然后挂载`proc`文件系统的简写。

省略`fork`选项会导致奇怪的 shell 行为，因为 shell 通常会派生出新的进程，这些进程现在是与主进程不同的名称空间。

如果您给大多数参数(如`--pid`或`--mount`)添加一个文件名，您可以创建一个在进程间共享的持久名称空间。您还可以使用虚拟以太网适配器(veth 类型)或网桥将一个名称空间中的网络暴露给另一个名称空间。

## 安装和更多选项

另一个有用的隔离是在挂载表中。Linux 处理挂载的方式略有不同。您可以通过多种方式传播挂载。如果您想要完全隐私，您可以这样做，但您也可以在一个组内共享，或者跟踪其他组中的更改，但不传播您自己的更改。你可以在手册页上阅读更多[。](https://man7.org/linux/man-pages/man7/mount_namespaces.7.html)

有趣的是，由于名称空间是隔离的，普通用户在新的名称空间中有可能拥有准 root 权限。`--map-root-user`允许这样做，并且还打开了一个选项来拒绝用户调用`setgroups`，这可能允许他们获得提升的权限。

当然，还有更多。如果您已经安装了`util-linux`,只需请求`unshare`手册页来阅读更多内容。如果你想在程序中使用这些东西，这可能更容易想象，有一个`unshare`系统调用。使用`man 2 unshare`查看详情。请注意，您可以通过系统调用进行更多的控制。例如，您可以取消文件系统的关联。它与`clone`系统调用紧密相连，后者是`fork`的超级版本。

您可能会觉得有趣的是，进程的所有名称空间数据都出现在`/proc`中。例如，尝试:

```
sudo ls -l /proc/$$/ns/*
```

您将看到带有当前进程的不同名称空间信息的专用符号链接。例如:

```

lrwxrwxrwx 1 alw alw 0 Dec 8 07:29 /proc/2182630/ns/cgroup -> 'cgroup:[4026531835]'
lrwxrwxrwx 1 alw alw 0 Dec 8 07:29 /proc/2182630/ns/ipc -> 'ipc:[4026531839]'
lrwxrwxrwx 1 alw alw 0 Dec 8 07:29 /proc/2182630/ns/mnt -> 'mnt:[4026531840]'
lrwxrwxrwx 1 alw alw 0 Dec 8 07:29 /proc/2182630/ns/net -> 'net:[4026531992]'
lrwxrwxrwx 1 alw alw 0 Dec 8 07:29 /proc/2182630/ns/pid -> 'pid:[4026531836]'
lrwxrwxrwx 1 alw alw 0 Dec 8 07:29 /proc/2182630/ns/pid_for_children -> 'pid:[4026531836]'
lrwxrwxrwx 1 alw alw 0 Dec 8 07:29 /proc/2182630/ns/time -> 'time:[4026531834]'
lrwxrwxrwx 1 alw alw 0 Dec 8 07:29 /proc/2182630/ns/time_for_children -> 'time:[4026531834]'
lrwxrwxrwx 1 alw alw 0 Dec 8 07:29 /proc/2182630/ns/user -> 'user:[4026531837]'
lrwxrwxrwx 1 alw alw 0 Dec 8 07:29 /proc/2182630/ns/uts -> 'uts:[4026531838]'

```

这是一种有点晦涩的 Linux 主义，但是在你需要的时候会非常有用。即使您现在不需要它，它也是值得理解的，因为它可能会解决您的下一个开发挑战。当然，你可以在自己的虚拟机上运行你的程序，但是与简单明了地隔离你想要的东西相比，这是一个相当沉重的选择。即使是在 shell 脚本中。