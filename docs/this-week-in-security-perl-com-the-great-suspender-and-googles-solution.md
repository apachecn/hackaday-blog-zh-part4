# 本周安全:Perl.com，伟大的吊杆，和谷歌的解决方案

> 原文：<https://hackaday.com/2021/02/05/this-week-in-security-perl-com-the-great-suspender-and-googles-solution/>

[Perl 被盗](https://log.perl.org/2021/01/perlcom-hijacked.html)。至少在 perl.com 是这样。1 月 27 日，perl.com 域名未经合法所有者许可，被转让给了另一家注册服务商。第一个注意到黑客攻击的似乎是【xtaran】，他[在 Reddit 帖子](https://www.reddit.com/r/perl/comments/l6d8ws/perlcom_unfriendly_domain_take_over/)上提出了警告。适当的人很快注意到了，并再次开始了控制该领域的过程。似乎[其他几个不相关的域名也在同一次攻击](https://news.ycombinator.com/item?id=25940240)中被盗。

我看到了一些关于域名被盗的理论。随着多个域名的迁移，最初似乎是注册服务商受到了某种程度的影响。另一名受害者被告知，已经提供了一套官方文件，“证明”攻击者是该域名的合法所有者。无论如何，损害正在慢慢消除。Perl.com 又一次掌握在合适的人手中，12 月发布的合适的 SSL 证书就是证明。

## 伟大的吊杆，悬挂着

本周周四，迎接我的是一个特别令人讨厌的惊喜。我开始依赖的一个 Chrome 扩展因包含恶意软件而被谷歌移除。伟大的悬挂器自动休眠未使用的标签，节省 ram 和处理器周期，否则这些周期将花费在 150 个真正应该是书签的打开标签上。这里发生了什么？

我要指出的是，我对安装扩展非常小心。它是由第三方编写的代码，通常很难检查，并且可以查看和修改您访问的网站。您可以管理一个扩展可以访问哪些站点，但是对于像吊杆这样的工具，它本质上需要访问所有的站点。解决方案是使用开源扩展，对吗？“嗯是的，但实际上不是。”毕竟，吊杆是开源的。上面的链接指向该项目的 Github 页面。在那份回购协议中，你会发现去年的一份公告，即创始开发者已经完成了项目，并将版权出售给一个不知名的第三方，后者接管了维护权。如果这听起来很熟悉的话，这让人想起了[事件流的崩溃](https://www.zdnet.com/article/hacker-backdoors-popular-javascript-library-to-steal-bitcoin-funds/)。

目前还不清楚谷歌到底发现了什么恶意行为导致该扩展被取消，但更仔细地研究该项目可以发现，早在 2020 年 10 月就存在潜在问题。对扩展的添加引入了从远程服务器执行代码，这绝不是一个好主意。不管怎样，最初的维护者已经发表了声明，为新的所有者辩护，并暗示这是一个无心的错误。

这里的教训是？仅仅确认一个扩展选中了“开源”框是不够的。确保有一个活跃的社区，并且没有 6 个月前的错误报告详细说明潜在的恶意活动。

## Libgcrypt

并不是每天你都能看到一个开发者发出通知说每个人都应该停止使用他的最新版本。这正是 Libgcrypt 1.9.0 所发生的事情。我们在谷歌零项目[的朋友在代码](https://bugs.chromium.org/p/project-zero/issues/detail?id=2145)中发现了一个极其严重的漏洞。这是在解密过程中发生的缓冲区溢出，甚至在签名验证之前。由于 libgcrypt 在许多 PGP 实现中使用，因此后果可能很严重。收到一封加密的电子邮件，一旦你的客户解密，代码就开始执行。幸运的是，已经发布了修复该问题的更新。

## 安卓僵尸网络

一个新的僵尸网络正以一种特殊的方式瞄准 Android 设备——[寻找暴露在互联网上的开放 ADB 调试端口](https://www.zdnet.com/article/android-devices-ensnared-in-ddos-botnet/)。Google 明确表示，ADB over the network 是不安全的，应该只用于开发目的，并且在受控网络上使用。令人震惊的是，如此多的供应商发布了带有这种服务的硬件。除此之外，令人惊讶的是，如此多的人给他们的 Android 设备公开 IP 地址(或不在防火墙后面的 IPv6 地址)。名为 Matryosh 的僵尸网络有另一个独特的功能，因为它使用 Tor 进行命令和控制功能，使其更难跟踪。

## 谷歌开源安全解决方案

谷歌在他们的开源博客上发布了[一篇文章，概述了他们开源项目安全的新框架。“了解、预防、修复”是他们对这项新工作的命名，而且肯定是管理层写的，因为里面充满了流行词汇。最有趣的元素是他们对关键软件的目标。他们发现了一些问题，比如单个维护者将糟糕的代码推进到项目中的能力，以及匿名维护者可能不是一个好主意。看看这些想法如何发展，以及谷歌将如何帮助开源社区实现它们，将会很有趣。](https://opensource.googleblog.com/2021/02/know-prevent-fix-framework-for-shifting-discussion-around-vulnerabilities-in-open-source.html)

## 微软在我的 Pi 里

最后，我被[一篇感叹默认 Raspberry Pi 操作系统映像中包含 VSCode 库](https://www.cyberciti.biz/linux-news/heads-up-microsoft-repo-secretly-installed-on-all-raspberry-pis-linux-os/)的文章逗乐了。他确实提出了一些合理的观点。其中，每次检查新的更新时，你都会向微软的服务器发送一个 ping。

更重要的一点是，官方的 VSCode 二进制文件中添加了遥测代码，这些代码不在开源库中。它在做什么？你不知道。但是这很可能违反了欧洲法律。

想使用 VSCode，但对向 Microsoft 发送信息不感兴趣？ [VSCodium 是个东西](https://vscodium.com/)。