# 在 Go 中从头开始构建更快的 Rsync

> 原文：<https://hackaday.com/2022/06/01/building-faster-rsync-from-scratch-in-go/>

对于两台计算机之间的快速文件传输，SCP 是一个很好的程序。但是，对于更复杂的大型或常规备份，首选工具是 rsync。它速度更快，效率更高，适用于更广泛的环境。尽管有它的好处，[Michael Stapelberg]觉得它有一个主要的弱点:它是一个用 C 编写的工具。[Michael]从哲学上反对用 C 编写的程序，[所以他开始在 Go 中从头实现 rsync，而不是用](https://media.ccc.de/v/gpn20-41-why-i-wrote-my-own-rsync)。

[迈克尔]决定处理这个项目的过程是复杂的。他的 ISP 最近将他的互联网连接升级到 25 Gbit/s，这意味着他的定制路由器是他网络的瓶颈。为了解决这个问题，他将他的路由器迁移到一台带有多个 25 Gbit/s 网卡的 PC 上。为了充分利用现在理论上可用的速度，他开始使用一种叫做 gokrazy 的工具，这种工具可以把用 Go 编写的应用程序变成他们自己的设备。这意味着不需要安装一个完整的 Linux 发行版来处理特定的任务(比如路由器)，在计算机上加载的唯一东西本质上是 Linux 内核、Go 编译器和库，然后是 Go 应用程序本身。

有了一个新的路由器，其硬件能够支持这些快速速度，并且只运行用 Go 编写的软件，最后一步是构建 rsync 来支持他在网络上的任务。这意味着 rsync 本身需要在 Go 中从头开始构建。一旦[Michael]完成了这个最后的任务，他发现他的 rsync 实现实际上比 C 中构建的版本快得多，这要归功于 Go 语言中发现的现代化，以及他的路由器没有运行与标准 Linux 发行版相关的所有 cruft 的事实。

对于这种规模的软件项目，我们发现对于我们任何人试图解决的任何问题，[Michael]的一步一步的过程都值得注意。不仅如此，重构一个像 rsync 这样的基础工具本身就是一项复杂的任务，更不用说仅仅为了提高网络速度而创造它了，这已经超出了我们大多数人已经认为的惊人的速度。我们忽略了这个版本的很多细节，所以我们强烈建议在下面的视频中看看他的演讲。

感谢[sarinkhan]的提示！

 [https://www.youtube.com/embed/wpwObdgemoE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/wpwObdgemoE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

