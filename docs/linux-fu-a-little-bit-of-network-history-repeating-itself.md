# Linux Fu:一点点(网络)历史重演

> 原文：<https://hackaday.com/2021/04/26/linux-fu-a-little-bit-of-network-history-repeating-itself/>

如今，嵌入式系统通常都有网络，这使得它们变得更加复杂。网络通常是相当不确定的，有各种各样奇怪的情况。例如，当您的公共访问拾放机在 Hackaday 上被记录时，您的流量突然激增 50 倍，您的网络堆栈如何处理它？虽然网络测试没有灵丹妙药，但有一些技巧可以让它变得更容易，其中之一就是`tcpreplay`实用程序，它允许您记录复杂的网络流量，然后以各种方式回放。这有很多好处，尤其是如果你设法抓住了偶尔引发不良行为的那一点。能够按需回放可以大大加快诊断速度。

## 大意

你可能知道`tcpdump`允许你从一个网络接口抓取数据包并保存到一个文件中。如果您喜欢 GUI，您可能会使用 Wireshark，它使用相同的底层库(`libpcap`)来获取数据。事实上，您可以使用`tcpdump`捕获数据，并使用 Wireshark 查看，尽管也有其他工具如`tcptrace`或`Ngrep`可以处理输出。

虽然在没有工具支持的情况下，该命令的输出可能有点模糊，但是一个名为`tcpreplay`的程序可以获取这些数据，并以各种方式反馈回来。当然，您可以首先修改文件，有工具可以使这变得更容易，如果您需要，您可以手动或使用各种工具之一来创建自己的网络流量。这个过程通常被称为“数据包制作”

## 获取数据

有时使用`tcpdump`是一个例子，说明一件好事怎么会太多。如果您只是从某个特定的网络设备上抓取所有内容，您将会得到大量的数据文件:

```
tcpdump -i eth0
```

通常，您会希望以不同的方式限制数据。例如:

```
tcpdump src 192.168.1.111   # data from .111
tcpdump dst 192.168.1.111   # data to .111
tcpdump host 192.168.1.111  # data to/from .111
```

其他常见的过滤器包括用于特定子网或“端口”的“net”，甚至是像“arp”或“ip6”这样的协议您可以这样组合这些:

```
tcpdump port 8088      # traffic on port 8088
tcpdump dst port 8080  # traffic to port 8088
```

端口也可以有范围(80-89 ),还有许多其他过滤器，包括数据包大小限制。您可以用“或”和“和”来连接条件有很多东西需要学习，您可以在 [`tcpdump`手册页](https://www.tcpdump.org/manpages/tcpdump.1.html)上阅读更多内容。

`tcpdump`的确切输出取决于所使用的协议。您也可以添加-X 或-XX 选项来获得十六进制转储。

所以现在你有一个文件，里面有一些有趣的网络数据。出于调试目的，如何重复它？

## 大回放

这就是`[tcpreplay](https://github.com/appneta/tcpreplay)`发挥作用的地方。简单地说，它易于使用:

```
tcpreplay -i eth0 traffic.pcap
```

然而，你可能需要更多的控制。例如，默认情况下，重放速度与最初发生的速度相同。但是，您可以添加“–Mbps”选项来强制特定的流量。您甚至可以使用“–Mbps = 0”来使数据包之间完全没有延迟。

还有其他性能选项。如果可能的话，“-K”选项将整个捕获文件读入内存以提高性能。如果您使用“–loop”选项来重复播放，这可以带来很大的性能优势。

在一些极端的情况下，您可能想要真正使网络接口饱和以进行测试。有一些特殊的驱动程序`tcpreplay`可以使用，允许它直接写入网络硬件，尽管这样做会在播放时禁用正常的网络操作。

## 编辑

有时，您希望在不实际更改文件的情况下，对捕获文件中的流量进行细微的更改。basic 程序有几个选项可以提供帮助。例如，“–unique-IP”选项将使程序在每次循环中改变数据包的唯一性。

然而，有时你需要更多的控制。这个`tcpreplay-edit`程序可以做很多改变。例如，它可以重新映射 TCP 或 UDP 端口。它还可以随机分配 IP 地址，删除广播，并进行其他动态更改。

作为一个实际的例子，您可以记录客户机和服务器之间的会话。为了重现服务器的行为，您可能希望从文件中剥离服务器的响应并重写 MAC 地址，这样客户机现在就是运行`tcpreplay`的机器。

这些工具非常强大，就像许多强大的工具一样，可以用于好的或坏的目的。有这么多的选择，但您会发现，如果您只是开始尝试一些“玩具”案例，并花几分钟时间阅读每个手册页，您将能够找到监视和重放网络流量的方法，以帮助解决下一个棘手的网络问题。