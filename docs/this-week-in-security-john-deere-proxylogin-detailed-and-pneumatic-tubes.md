# 本周安全:John Deere、ProxyLogin Detailed 和气动管道

> 原文：<https://hackaday.com/2021/08/13/this-week-in-security-john-deere-proxylogin-detailed-and-pneumatic-tubes/>

我们已经报道了[维修权利的传奇](https://hackaday.com/2021/08/11/should-you-be-able-to-repair-it-we-think-so/)，其中一家已经变得相当臭名昭著的公司是 John Deere。管理不善的互联混乱的另一面是安全问题。这个故事的开头具有一定的讽刺意味:有人注意到 John Deere 设备根本没有任何简历。一个正常人可能会认为这一定意味着他们的产品是超级安全的，但是一个安全研究员知道一些更有趣的事情正在发生。我们的老朋友[病态代码]、[约翰·杰克逊]和许多其他人认为这是一个明确的迹象，表明有大量的漏洞有待发现，[看来他们是正确的](https://sick.codes/being-root-on-two-agriculture-companies-in-good-faith-maxing-out-the-john-deere-operations-center-worldwide-and-case-industrial-in-brazil/)。

![](img/1eef77e3d6cf7938996e2140382d3485.png)

Remote Access and Code from 2014…

漏洞包括少量跨站点脚本攻击、通过请求走私绕过认证、错误配置的安全性、SQL 注入、RCEs 等等。总之，这些漏洞允许完全控制 John Deere 系统，包括操纵连接到系统的所有设备的能力。

在 Defcon 演示期间，链接如下，[病态代码]回忆起他们意识到他们正在解决一个重要问题的时刻。一位投稿人没有抱怨没有为发现的漏洞获得报酬，而是简单地指出他重视有食物吃。对 JD 设备的协同攻击可能会给全国的许多农场带来大问题。

由于缺乏供应商的认真回应，他们最终联系了 CISA。CISA 认真对待这一威胁，问题开始得到解决。这不仅仅是一家公司的问题。案例中的类似问题也已得到解决，这意味着其他供应商也有类似的问题，这些问题仍在解决过程中。

## 八进制 IPs 再次出击

当我们在谈论[病态代码]和他的研究人员的快乐乐队，有几个不正确的八进制格式的 IP 地址解析的实例公布。那就是[Rust STD::net](https://sick.codes/sick-2021-015/)和[Golang net](https://sick.codes/sick-2021-016/)库，这两个库只是去掉了 ip 地址的前导零。在这两种情况下，解决方法都是将其视为无效地址。为什么会有问题？因为可以用偷偷摸摸的 IP 地址，像`0127.0.0.1`。一个八进制感知库将此视为`87.0.0.1`，而一个有此漏洞的库将其视为 localhost。当 web 服务的不同部分同时使用这两种方法时，真正的问题就出现了。如果您可以控制或欺骗其中一个神奇的地址，您就可以连接到该服务并拥有特权，就像您使用内部 IP 一样。有关更多信息，请参见[DEF CON 关于此问题的讨论](https://www.youtube.com/watch?v=_o1RPJAe4kU)。

## 交换资源

记得 ProxyLogon 吗？这就是我们自今年年初以来一直在共同应对的微软 Exchange 攻击。终于到了讲述剩余故事的时候了。继续我们的会议报道， [[Orange Tsai]详细描述了这个漏洞，并宣布了黑帽](https://www.blackhat.com/us-21/briefings/schedule/index.html#proxylogon-is-just-the-tip-of-the-iceberg-a-new-attack-surface-on-microsoft-exchange-server-23442)的两个新的交换漏洞，包括另一个通过端口 443 通向 RCE 的链。如果这还不够的话，[已经有利用这个新漏洞的主动攻击](https://www.bleepingcomputer.com/news/microsoft/hackers-now-backdoor-microsoft-exchange-using-proxyshell-exploits/)。

这项新研究源于 Exchange 2013 中的一项架构变化，其中 web 服务被分为前端和后端。这有各种各样奇怪的结果，比如后端默认监听所有接口。另一个？前端不会对传入的请求验证主机，因此攻击者可以在其中插入任意文本。这包括完全不同的主机名和端口，以及意外的字符。将这些正确地放在一起会导致任意的 SSRF——攻击者可以指定公共互联网上的任何端点，或者后端本身。一旦正常的前端到后端流程遭到破坏，就很容易滥用内部端点来获得任意写权限和 RCE。简而言之，这就是 ProxyLogon 攻击。

新的 RCE 被称为 [ProxyShell](https://peterjson.medium.com/reproducing-the-proxyshell-pwn2own-exploit-49743a4ea9a1) 。它滥用预授权自动发现端点，旨在为客户端启用自动配置。将所需的端点附加到有效的自动发现请求可用作 SSRF 工具。攻击是使用此 SSRF 向/powershell 端点发出请求。结合作为草稿上传的 webshell 有效负载，这导致了另一个预授权 RCE。谢天谢地，这些攻击已经被修补，但仍有太多的系统尚未更新。

 [https://www.youtube.com/embed/5mqid-7zp8k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/5mqid-7zp8k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



## 脉冲安全被焦油击败

这个故事从 CVE-2020-8260 开始，这是 Pulse Connect 安全设备中的一个任意文件写入漏洞，在该漏洞中，上传的配置在提取时没有进行路径横向检查。恶意的 tar 文件可以通过`./../`路径将文件放在任何地方。这个问题在 2020 年得到了解决，但几个版本之后，CVE-2021-22900 被披露并得到了解决。这是一个奇怪的类似问题，NCC 集团[的【里奇·沃伦】决定调查](https://research.nccgroup.com/2021/08/05/technical-advisory-pulse-connect-secure-rce-via-uncontrolled-archive-extraction-cve-2021-22937-patch-bypass/)。最初的修复增加了一个`validateTarFile`功能，这似乎是一项非常出色的工作。它检查`../`模式、符号链接或硬链接。最重要的是，它有一个允许文件的白名单。这将是一个完美的解决方案，只要每次上传档案时都使用它。不幸的是，这种健壮的解决方案仅在上传配置文件时使用。第二个修正是将对`validateTarFile`的调用添加到所有其他上传函数中。

有了这种理解，自然要问的问题是是否每个文件上传环境都被适当地清理了。既然我们在讨论这个问题，你可能已经猜到有什么遗漏了。上传配置文件时，POST 消息的参数定义上传类型。剖析器数据库的处理方式不同，并且该代码路径不包括验证函数，这导致了 CVE-2021-22937。看起来这个代码路径在正常使用中是不可访问的，但是修改请求参数是微不足道的。这一系列漏洞仅限于对设备具有管理员访问权限的攻击者，大大降低了其严重性。也就是说，对底层文件系统的访问打开了一个持续威胁的全新世界。取决于它是如何实现的，这样的 rootkit 可以在工厂重置后继续存在。

## API 测试 101

Detectify 的好人们出版了一本有趣的测试 web APIs 的初级读本。这篇文章的前半部分致力于使用[邮差](https://www.postman.com/downloads/)进行这项研究。它看起来是一个有用的工具，但不幸的是，它似乎是封闭源代码的。本文的第二部分涵盖了 web APIs 中的一些常见问题以及缓解这些问题的思路。这里讨论了一些明显的缺陷，比如私有 API 意外地暴露给了公众。另一方面，有一些很好的技巧可以用来寻找更隐蔽的缺陷，比如 XXE 注入(XML 外部实体)。总之，它值得一读，特别是如果你不反对将一个闭源工具作为你的工具箱的一部分。

## 气动管系列

你可能最熟悉银行或药店免下车餐馆(或观看《未来》时)的气动管道系统(PTS ),但它们也广泛用于医院和其他地方。Armis 的研究人员刚刚公布了 PwnedPiper ，这是 Swisslog Healthcare 的 PTS 实施中的一系列问题。最糟糕的问题之一？他们的控制面板是 Linux 系统，运行 2.6.35 内核。这是 10 年前的内核。还记得上周[抨击谷歌安全的博客](https://security.googleblog.com/2021/08/linux-kernel-security-done-right.html)吗？这是他们心目中的那种无稽之谈。

系统的其余部分也一样糟糕，一个开放的 telnet 服务监听连接，一个所有设备通用的硬编码密码。多个内存损坏错误都允许 RCE，主要通信协议是未加密和未认证的，更不用说基于 UDP。最后，固件升级过程也是基于同样的协议，根本没有固件签名功能。简单来说，如果你可以访问运行这个 PTS 的以太网，你就可以轻松地拥有整个系统。

如果真的被利用，情况会有多糟？想想看，不仅生物样本通过这个系统传送，药物也是如此。人们可以想象打乱目的地会造成多大的麻烦。更恶意的攻击者可能会利用这种攻击来窃取或替换药物。听起来像是《碟中谍》中的一个情节，但是事实有时比小说更奇怪。

## 最后一刻的头条新闻

Foxit PDF [阅读器最近发布了 11.0.1](https://www.foxit.com/support/security-bulletins.html) ，修复了一大堆问题，包括 8 个可能导致 RCE 的独立简历。如果你是这款广受欢迎的 Adobe 替代品的用户之一，请确保你已经更新了！

就像我们需要其他东西来中断电子供应链一样， [Gigabyte 受到了勒索软件](https://www.bleepingcomputer.com/news/security/computer-hardware-giant-gigabyte-hit-by-ransomexx-ransomware/)的攻击，另外还有 112GB 的数据被泄露的威胁。更糟糕的是，据报道，许多数据都在 NDA 名下，如果公开，可能会给技嘉带来进一步的后果。到目前为止，还不知道赎金是多少。

又一个我们以为已经死亡的故事复活了。还有另一个打印假脱机程序 0 天。这是另一个与指向打印相关的漏洞，但这次是针对试图使用恶意远程打印机的机器。以前的这种漏洞是不可访问的，只要点击打印被禁用，这是默认设置。[微软的建议没有把它列为这个问题的解决方法](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-36958)。看起来这在标准配置下是可行的。雪上加霜的是，[报告研究人员早在 2020 年 12 月](https://twitter.com/offenseindepth/status/1425574625384206339)就披露了这个缺陷。