# 本周安全:死亡之袋、漫步者、待售的 HIBP 和 Oracle Weblogic——又来了！

> 原文：<https://hackaday.com/2019/06/21/this-week-in-security-sack-of-death-rambleed-hibp-for-sale-and-oracle-weblogic-again/>

当考虑安全研究公司时，网飞不是第一个想到的名字，但他们在内容交付系统中大量使用 FreeBSD，并因此进行安全研究。不出所料，他们今年的第一个安全公告覆盖了一个 FreeBSD 漏洞，这个漏洞碰巧也影响了过去 10 年的 Linux 内核。此漏洞使用 SACKs 和奇数 MSS 值使服务器内核崩溃。

为了理解选择性 ack，我们需要后退一步，看看 TCP 连接是如何工作的。TCP 连接提供有保证的交付，以确认(ACK)数据包的形式实现。我们认为 TCP 连接对于每个数据包都有一个专用的 ACK 包。实际上，操作系统尽最大努力避免发送“裸”ACK 包，并将多个 ACK 组合在一个包中。ACK 只是数据包报头中的一个标志，与收到的字节总数相结合，可以包含在普通数据包中。接收数据的 ACK 会尽可能与反向传输的数据包一起发送。

这种方法的一个问题是，当传输失败时，不清楚哪个包被丢弃，必须重新传输多个包。处理 ack 的另一个策略是使用选择性 ack 或 SACKs。SACK 将包括 ACK 标志、总字节数以及 TCP 序列号。当数据被丢弃时，SACK 数据包会准确地指出哪些数据包丢失了。

另一个需要理解的术语是最大数据段大小(MSS)。该值通常在初始 TCP 握手期间指定，并指定在单个 TCP 数据段中可以传输多少数据。MSS 设置为较低的数字通常会导致数据被分割成多个数据段。

网飞概述了与 SACK 相关的几个问题，但最严重的漏洞是当攻击者建立到 Linux 或 FreeBSD 服务器的 TCP 连接，并将 MSS 设置为尽可能低的值时触发的。传输数据后，攻击者发送一系列 SACK 数据包，请求重新传输特定的多个数据包。这种特制的数据包系列会导致多个碎片消息溢出服务器的传出缓冲区。这种攻击似乎不会导致代码执行，但它会立即导致内核崩溃，从而使目标机器离线。

修复该问题的补丁已经发布，~~，但是还不能在实时系统上轻松安装。这些补丁还没有成为正式内核发布的一部分，但大多数发行版已经移植了这些补丁，并提供了更新。要了解更多信息，请看下面一位匿名评论者的非常有用的评论。~~

作为一种变通办法，网飞建议要么完全禁用 SACK，要么过滤 MSS 值非常低的数据包。有关这些缓解措施的更多信息可在他们的公告中获得。

### 漫步

[![](img/a65b7d534a959d5dd5c4870bd307f502.png)](https://hackaday.com/wp-content/uploads/2019/06/rambleed-10-1.png) 基于 Rowhammer 的概念， [Rambleed](https://rambleed.com/) 攻击其他进程的内存，但通过读取该内存，而不仅仅是写入它。就像 [Rowhammer](https://googleprojectzero.blogspot.com/2015/03/exploiting-dram-rowhammer-bug-to-gain.html) 一样，其核心思想是现代 RAM 的密度如此之大，以至于单个位对附近的位产生了可检测的影响。Rowhammer 允许攻击者翻转附近的位，即使它们可能属于不同的进程，甚至是内核本身。

Rambleed 依赖于内存的物理布局——它本质上是一个二维网格。上面和下面的位对给定位的位翻转有影响。如果攻击者可以控制一行内存，就可以在该行的一个位上发起行锤攻击。通过测量攻击的有效性，可以从统计上确定上下位的状态。

历史上，这种性质的物理 RAM 攻击被 ECC 内存击败。Rambleed 的研究人员提出了两种克服 ECC 的方法。第一种是翻转多个位，以便 ECC 算法仍然将模式评估为正确的。第二种技术是定时攻击，纠错读取比未纠错读取花费的时间长得多。因为翻转位的存在与否足以确定目标位的值，所以 ECC 机制失效。作为他们的绝招，作者通过从 OpenSSH 7.9 服务器恢复 RSA-2048 密钥来演示 Rambleed。

### 我被卖了吗？

首先，如果你还没有，去看看[我被 pwn 了吗](https://haveibeenpwned.com/)。给网站一个电子邮件地址，它将返回一个帐户使用该电子邮件地址的网站列表。跟踪你的账户在哪里被刮和暴露是非常有用的。虽然有些命中是良性的，比如你的电子邮件地址是从公共 Github 数据中刮出来的，但你可能只是发现了一个泄露了重要密码或其他数据的旧论坛或服务。

尽管这项服务很有用，但令人惊讶的是看到[一个虚拟的待售标志](https://www.troyhunt.com/project-svalbard-the-future-of-have-i-been-pwned/)出现了。[Troy Hunt]独自经营这个网站已经超过 5 年了。他现在测量的流量是以百万计的，记录的数量是以十亿计的，最近他顿悟到，除非做出改变，否则个人的倦怠即将出现。他正在寻找一家母公司或公司来收购 HIBP，坚持他的核心原则，并让他做出一些改变来保持这艘船的航行。

### 零天！

Oracle Weblogic 正成为 [Java 反序列化攻击](https://medium.com/@knownsec404team/knownsec-404-team-alert-again-cve-2019-2725-patch-bypassed-32a6a7b7ca15)的目标。如果这听起来很熟悉，那是因为[我们不久前在这里](https://hackaday.com/2019/05/01/this-week-in-security-facebook-hacked-your-email-cyber-on-the-power-grid-and-a-nasty-zero-day/)谈论过它。

考虑到当前这个问题的重现，4 月份关于漏洞的评论似乎特别恰当。[Rob VandenBrink]观察到，Oracle 对该问题的解决方案只是将特定的攻击媒介列入黑名单，而不是采取措施修复底层的反序列化问题。

Firefox 在上周发布了两个点版本，修补了两个漏洞，据报道,[在针对比特币基地员工的攻击中被频繁使用。还没有公布所有的细节，所以期待下周更多的细节。现在，只要确保你的 Firefox 版本至少是 67.0.4。](https://arstechnica.com/information-technology/2019/06/potent-firefox-0day-used-to-install-undetected-backdoors-on-macs/)