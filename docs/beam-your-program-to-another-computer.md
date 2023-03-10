# 把你的程序传送到另一台计算机上

> 原文：<https://hackaday.com/2020/04/28/beam-your-program-to-another-computer/>

如果您已经在 Linux 或 Unix 中编写了很多程序，那么您可能会遇到 fork 系统调用。对 fork 的调用会导致您现有的流程——关于它的一切——突然分裂成两个完整的副本。但是它们运行在同一个 CPU 上。特里斯坦·休姆有个主意。他希望有一个调用，telefork，可以在 Linux 集群中的不同机器上创建副本。他放不下这个想法，最后[自己写代码](https://thume.ca/2020/04/18/telefork-forking-a-process-onto-a-different-computer/)来做。

如果你仔细想想，这个问题的一部分很容易，而另一部分很难。例如，创建流程代码和数据的副本并不难。因为目标是一个集群，所以机器基本上是相同的——这并不是说您试图将一个 Linux 进程移动到一个 Windows 机器上。

然而，一个真正的 fork 确实给了新进程一些棘手的东西，比如开放的 TCP 连接。[Tristan]暂时回避这些问题，但有办法在未来让事情变得更好。他构建了其他开源项目中做类似事情的例子，包括[分布式多线程检查点](http://dmtcp.sourceforge.net/) (DMTCP)。这项任务需要很好地理解操作系统是如何安排进程的。

除了让 telefork 更强大之外，[Tristan]还有一些“更疯狂”的想法，比如一次向多台机器发送数据，或者使用虚拟内存分页只在需要时复制内存。他甚至希望允许一个进程认为它有许多线程，但是其中一些运行在不同的 CPU 上。这意味着一个程序可以“认为”它有成百上千个内核。看起来细节上有很多问题，但是理论上是可行的。

这可能正是你的[树莓派集群](https://hackaday.com/2020/04/24/raspberry-pi-cluster-shows-you-the-ropes/)需要的东西。不过，可能对你的 [ESP32 集群](https://hackaday.com/2018/01/14/imagine-a-cluster-of-esp32s/)没那么有用。