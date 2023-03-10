# 从计算模块中获得超过 4Gbps 的性能 4

> 原文：<https://hackaday.com/2020/11/09/getting-over-4gbps-out-of-a-compute-module-4/>

对于普通的家庭游戏玩家来说，100 Mbit/s 的老式以太网只是刚刚开始成为一个瓶颈，因为像 4K 视频流这样的东西开始需要更多的带宽。然而，一如既往，有些人希望挑战可能的极限。[Jeff Geerling]就是这样一位操作员，[他着手在 Raspberry Pi 计算模块 4 上最大化网络吞吐量。](https://www.youtube.com/watch?v=a-0PeuPINiQ)

构建从利用新的 Raspberry Pi 计算模块上的 PCI-Express 2.0 单通道接口开始。连接到英特尔四端口千兆以太网卡，并结合板载千兆位 E 端口，[Jeff]能够毫不费力地获得 3.0 Gbit/s 的设置。然而，他想要更多，并开始寻找他被阻止的地方。原来，处理网络数据包的守护程序`ksoftirqd`只能在树莓 Pi 4 上的一个内核上运行，并且它在这个数据速率下已经达到极限。CPU 超频有所帮助，最高速率可达 3.4 Gbit/s。

进一步的分析表明，板载接口仅贡献 200 Mbit/s，英特尔卡的最大速度为 3.2 Gbit/s。对于后者，这是由于 PCI-E 接口的限制。然而，对于前者，[杰夫]知道还有更多的可用。诀窍是重新编译 Linux 内核，允许内部接口能够设置使用更高的最大传输单位。这使得每次网络传输可以承载更多的数据，而不会增加额外的 CPU 负载。由于内部接口和外部卡都设置为 9000 的 MTU，Pi 能够吐出灼热的 4.15 Gbit/秒。好奇的人可以在 Github 上找到黑客攻击的细节。

这种技术对普通用户来说没什么好处，尽管[Jeff]表示他有一些有趣的应用。他还在考虑 10 Gbit 卡能实现什么，我们迫不及待地想看到这一点。如果您想了解更多关于计算模块的特性，包括一些布置您自己的板的技巧，[请查看我们的评论](https://hackaday.com/2020/10/19/new-raspberry-pi-4-compute-module-so-long-so-dimm-hello-pcie/)。休息后的视频。

 [https://www.youtube.com/embed/a-0PeuPINiQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/a-0PeuPINiQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



【感谢 Baldpower 的提示！]