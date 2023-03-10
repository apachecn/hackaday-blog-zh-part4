# 本周安全:DNS DDOS，15 岁的 Bug 的复仇，等等

> 原文：<https://hackaday.com/2020/05/22/this-week-in-security-dns-ddos-revenge-of-the-15-year-old-bug-and-more/>

另一种 DDOS 放大技术最近刚刚被披露，[nxn stack](http://www.nxnsattack.com/)(此处为[技术论文](http://www.nxnsattack.com/shafir2020-nxnsattack-paper.pdf))可用于攻击 DNS 服务器。

我们已经在之前[讨论过扩增攻击。简短的解释是，一些 UDP 服务，如 DNS，可以被滥用来从 DDoS 攻击中获得更多的好处。攻击机器发送这样的消息:“你好，谷歌 DNS，这是黑客服务器。能不能给我发一个真正大的 DNS 响应包？”如果 DNS 响应大于请求，那么整体攻击就会更大。衡量有效性的标准是放大系数。攻击机器每发送一个字节的 DDoS，实际上有多少字节是发送给受害机器的？例如，](https://hackaday.com/2019/09/20/this-week-in-security-zeroconf-strikes-again/) [Mirai 未来组合](https://www.cloudflare.com/learning/ddos/glossary/mirai-botnet/)的放大系数大约为 2.6。

NXNSAttack 的理论每字节放大系数为 163。这不是一个遗漏的小数点，这有可能是一个相当棘手的问题。

为了实现攻击，坏人需要控制一个对自己的域有权威的域名服务器:`evil.com`。然后，一个无辜的 DNS 被要求提供邪恶子域中随机机器的 IP 地址。由于无辜的 DNS 从未见过这个名字，它向根`.com`服务器询问邪恶的 DNS 服务器(`ns1.evil.com`)的 IP 地址，然后去那里询问。

正常情况下，邪恶的 DNS 服务器会用自己域中机器的 IP 地址来响应，故事会圆满结束。但是在这里，邪恶的域名服务器用目标域中许多“域名服务器”的地址进行响应，所有这些都是为了产生流量而发明的，并告诉无辜的 DNS 服务器去请求它们:`nslgb7vX.sucker.com`和`nseHOiF.sucker.com`等等。放大来了。

许多 DNS 解析器会查找它收到的每个“域名服务器”的 IP 地址，并且会并行执行，因为在正常情况下，这些 IP 会被缓存，它们可以一次扫描整个域的 DNS 服务器集，再也不用询问了。因此，无辜的 DNS 向根`.com`服务器请求目标的权威服务器`ns1.sucker.com`的 IP 地址，它将在那里查找所有假冒域名服务器的 IP 地址。

但是由于所有的“域名服务器”名称都是随机的和伪造的，无辜的解析者被愚弄了，用这些伪造的域名服务器的 IP 地址请求`ns1.sucker.com`。实际上，这会使 DNS 请求成倍增加:10-20 倍是可能的。完全攻击使用来自邪恶名称服务器的两个阶段的重定向来基本上平方请求的数量，这就是为什么它们在实践中以 163 的因子结束。在这种情况下，来自少数恶意机器的流量可以迅速淹没受害者的基础设施。

NXNSAttack 是私下透露给少数 DNS 供应商的，因此有限的缓解措施已经可用。运行递归 DNS 服务器已经是一项艰巨的任务，但是现在又多了一个陷阱需要小心。

### 长达 15 年的漏洞终于被利用了

一些漏洞显然是可利用的，并尽快得到修复。在其他情况下，代码在技术上可能是易受攻击的，但在某种程度上看起来几乎不可能被实际利用。人们很容易将这些视为无关紧要的问题而不予理会，也从不去解决它们。Qmail 包含三个缺陷至少有 15 年了，它是一个很好的例子，说明了为什么修复“不可利用的”问题很重要。

2005 年是 x86-64 机器首次面向大众的时代。某些编程假设在 32 位平台上是安全的，而在 64 位机器上不再有效，这并不奇怪。`Qmail`在编写时假设一个数组永远不会被分配超过 4 GB 的内存，这在 32 位时代是安全的。 [CVE-2005-1513、1514 和 1515](http://www.guninski.com/where_do_you_want_billg_to_go_today_4.html) 被报告并被驳回，因为在任何默认或合理的部署中，达到 4 GB 的限制被认为是不可能的。

快进到 2020 年 5 月 19 日，终于找到了利用这些漏洞的方法。易受攻击的代码也用在了`qmail-local`服务中，默认情况下，它并不局限于一个设定的内存量。巧尽心思构建的 4 GB 电子邮件可触发整数溢出，并导致远程代码执行。在完整的报道中有很多有趣的细节，所以请查看更多。

### 300，000 个易受攻击的 QNAP 设备

QNAP 生产的 NAS 设备很受专业用户的欢迎。除了简单的文件存储，这些 QNAP 设备还具有集成照片管理器、音乐播放器等功能。[黄士伟]发现了[三个独立的漏洞，它们可以链接在一起获得一个根 webshell](https://medium.com/bugbountywriteup/qnap-pre-auth-root-rce-affecting-450k-devices-on-the-internet-d55488d28a05) 。所以首先，任何 QNAP 用户，去检查更新！

既然您已经了解了最新情况，那么让我们深入了解一下漏洞链。首先，为与样本相册交互而设计的远程 API 无需身份验证即可访问。攻击者可以创建一个样本相册，并返回一个相册 ID。来自所创建的样本 ID 的信息用于创建一个请求，该请求可以读取文件系统上的任何文件，尽管未排序的文件名包含“`../../`”样式的字符。这用于读取应用程序登录令牌。

然后使用该令牌登录，另一对漏洞允许攻击者将 PHP 代码放入 web 文件夹中。剩下的工作就是在浏览器中访问新页面，然后运行注入的 PHP 代码。由于这些设备上的 web 服务器以根用户身份运行，注入远程外壳意味着整个设备受损。

### 百万美元挑战？

由 Epic Games 运营的 Houseparty 社交网络在 Twitter 上发起了一项挑战:提供关于 Houseparty 安全问题的诽谤活动的证据，他们将支付 100 万美元的赏金。

> 我们正在调查的迹象表明，最近的黑客谣言是由一个付费的商业诽谤活动传播，以伤害 Houseparty。我们悬赏 100 万美元给第一个向 bounty@houseparty.com 提供这一行动证据的人。
> 
> —house party(@ house party)[2020 年 3 月 31 日](https://twitter.com/houseparty/status/1244827034406121472?ref_src=twsrc%5Etfw)