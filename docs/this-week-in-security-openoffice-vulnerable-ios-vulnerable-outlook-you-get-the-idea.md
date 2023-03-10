# 本周安全:OpenOffice 易受攻击，IOS 易受攻击，Outlook…你明白了吗

> 原文：<https://hackaday.com/2021/10/01/this-week-in-security-openoffice-vulnerable-ios-vulnerable-outlook-you-get-the-idea/>

本周我们从[开始，一篇由【尤金·林】撰写的关于开始漏洞搜寻](https://medium.com/csg-govtech/all-your-d-base-are-belong-to-us-part-1-code-execution-in-apache-openoffice-cve-2021-33035-767fc7d6daf7)的好文章，以及关于 OpenOffice 处理 DBase 文件的一个问题的新闻。[Lim]决定专注于一种文件格式，并选择了受人尊敬的 dbase 格式，`.dbf`。这种数据库格式最终被广泛使用，并且在 Microsoft Office、Libreoffice 和 OpenOffice 中仍然得到支持。他用[的 Peach Fuzzer](https://gitlab.com/gitlab-org/security-products/protocol-fuzzer-ce) 设计了一个模糊方法，并通过测试一个非常简单的支持该格式的文件浏览器，发现了文件格式中的一些可能的漏洞。他设法在`dbfview`中实现了代码执行，但这还不够。

由于一个应用程序存在漏洞，[Lim]将注意力转向了 OpenOffice。他确切地知道自己在寻找什么，并马上找到了易受攻击的代码。缓冲区是根据指定的数据类型分配的，但是数据以不同的长度复制到这个缓冲区中，也是在 dbase 文件中指定的。简单的缓冲区溢出。把这变成一个真正的 RCE 利用需要一点时间，但这是可能的。该披露不包括完整的概念验证，但可能会很快进行逆向工程。

通常我们会告诉你去获取更新，但 OpenOffice 没有包含此修复的稳定版本。有一个[发布候选版本包含修复](https://dist.apache.org/repos/dist/dev/openoffice/4.1.11-RC1/)，但是目前世界上每个 OpenOffice 的稳定安装都容易受到这个 RCE 的攻击。漏洞报告早在 5 月 4 日就发出了，比完全披露早了 90 多天。而 OpenOffice 的分支 LibreOffice 呢？它肯定也很脆弱吧？没有。LibreOffice 在 2014 年的[例行代码维护中修复了这个问题。事情的真相是，当这两个项目分道扬镳时，](https://github.com/LibreOffice/core/commit/d4e64d030092984077021a9af9d281cd64c476bf)[真正理解代码库的程序员去了 LibreOffice](https://twit.tv/shows/floss-weekly/episodes/446) ，OpenOffice 从那以后一直严重缺乏程序员。我以前说过:用 LibreOffice，OpenOffice 已知不安全。

## iOS 困境

Denis Tokarev，又名[illusionfchaos]，已经受够了苹果的 bug bounty 计划，[披露了三个未修复的 iOS bug](https://habr.com/en/post/579714/)，远远超过了 90 天。但首先，在 14.7 版中，一个漏洞被修复了。在修复之前，设备上的任何应用程序都可以不受限制地读取分析日志，这是一个信息宝库。这次数据泄露被悄悄地修复了，苹果公司没有披露或承认。[丹尼斯]问，并被告知，他将被记入以后的版本。三个进一步的安全发布来了又去，仍然没有披露或信贷。

今年 5 月又报告了两起创伤，第三起发生在 3 月。它们是:允许应用程序读取 wifi 信息的权限旁路，应用程序确定安装了哪些其他应用程序的意外方法，以及允许应用程序访问包括用户认证令牌在内的各种东西的严重缺陷。在最老的问题上搁置了六个月后，[丹尼斯]给了苹果 10 天的最后期限，当这一天过去后，就把它们全部公布了。

[的后续帖子](https://habr.com/en/post/580272/)本身会很有趣，展示了一些通过应用商店的分析过程来隐藏恶意代码的技术。如果你期待尖端、先进的技术，准备好失望吧。苹果的分析会发现`NSClassFromString(["GKLocalPlayerInternal"])`访问的是苹果专有的 API。变通办法，真的可以避免检测？`NSClassFromString(["GKLoc","lPlayerInternal"].joined(separator: "a"))`这篇文章的其余部分与安全无关，但提出了一些关于 App Store 其他缺陷的有效观点。

## Netgear 的圈子

一些 Netgear 路由器附带了 Circle Parental Control 服务，虽然实际的网页过滤在默认情况下是关闭的，但更新服务会自动运行。【亚当】发现[这个更新过程](https://blog.grimm-co.com/2021/09/mama-always-told-me-not-to-trust.html)有两个问题，首先是使用 HTTP 获取更新。这使得攻击者能够在检查更新时执行中间人攻击，但是更新过程会检查更新 blobs 的有效签名。第二个问题是这些 Netgear 路由器使用的是 2007 年的`busybox`二进制文件。Busybox 是一个一体化的二进制文件，它为嵌入式设备提供了一组基本的 Unix 工具。一个这样的工具是`tar`，在 2007 年，一个重要的安全特性丢失了:绝对路径阻塞。

还记得 Circle update 进程在更新之前是如何检查二进制文件的有效签名的吗？二进制文件不是唯一更新的东西，还有一个数据库更新，它是作为一个 tarball 分发的，没有签名。由于不安全的 tar 处理，恶意的数据库更新可以覆盖系统启动脚本，也称为简单的 RCE。补丁是可用的，所以请检查您的设备是否受到影响。

## Outlook 自动发现

Guardicore 的研究人员发现了 Outlook 中的一个逻辑缺陷，该缺陷将一个旧漏洞变成了一个大问题。老问题[在 2016 年](https://www.theregister.com/2016/09/19/ms_exchange_alleged_bug)被披露，归结为一次加密降级攻击。如果试图使用 Exchange 自动发现的邮件客户端被强制连接到攻击者控制的服务器，则授权方法可能会降级为 Base64 编码的用户名/密码。当时，微软拒绝发布任何关于这种情况的指导或补丁。

Guardicore 发现的是自动发现 URL 域遍历逻辑中的一个缺陷。设置新的电子邮件地址时，Outlook 将尝试在新的地址域中查找 Autodiscover.xml 文件。所以对于像`user@mail.example.com`这样的地址，首先检查的位置是`[https://Autodiscover.mail.example.com/Autodiscover/Autodiscover.xml](https://Autodiscover.mail.example.com/Autodiscover/Autodiscover.xml)`。如果在该域中找不到自动发现文件，Outlook 将向上遍历，并检查`autodiscover.example.com`。到目前为止一切顺利。问题是逻辑并没有到此为止，还会检查`autodiscover.com`，这几乎可以肯定不是由邮件提供者控制的。每个顶级域名都存在这个问题。

Guardicore 的研究人员购买了 20 个`autodiscover.X`域名，并等待流量。在五天的时间里，他们收集了近 100，000 个不同的请求。令人震惊的是，这些请求包括使用基本身份验证(也称为明文)发送的帐户凭据。(好吧，是 Base64 编码，但那是编码，所以还是明文。)看来他们是在不小心进行授权降级攻击。最终用户的建议解决方案？在您的 DNS 提供商处阻止整个`autodiscover.TLD`域列表。

## XSS 标签

有点幽默的消息是，苹果的新 AirTag 有一个跨站点脚本缺陷。AirTag 的所有者可以设置一个自定义的消息和电话号码，显示给找到丢失设备的人。该电话号码字段目前尚未验证，因此您可以在其中放入任何内容，包括代码。finder 可能会扫描 AirTag，并因此被重定向到恶意站点。谢天谢地，这应该是一个相当容易的修复，实际上不是硬件问题。同样值得注意的是，这又是一个 0 天，这也是苹果对待研究人员不太好的方式的结果。

## 哎哟

还记得 5 月份的时候，苹果快捷方式一度破产吗？原来[是一名安全研究员【Frans Rosen】，正在研究苹果 CloudKit 服务的一个漏洞](https://labs.detectify.com/2021/09/13/hacking-cloudkit-how-i-accidentally-deleted-your-apple-shortcuts/)，这是一个数据存储框架。他发现支持多种 API，在访问或操作时，它们给出的结果略有不同。他在默认的快捷方式区域尝试了一个删除请求，并且成功了。本来不应该成功的，但是成功了。对于苹果用户来说，快捷方式在世界范围内都是垃圾。我可能对苹果的回应感到比我应该感到的更有趣。

> 谢谢你提供的信息。请停止…

最终发现并修复了三个 bug。在这种情况下，[Frans]对苹果安全团队印象深刻。他们确实为这三个问题支付了奖金，尽管他在找到其中一个问题时删除了整个世界的快捷方式。

## 剩余字节

EFF 正在到处淘汰 HTTPS，因为 HTTPS 现在实际上无处不在。该扩展将在 2022 年处于维护模式，并可能在那之后完全退役。不仅许多网站会自动将用户重定向到 HTTPS 连接，这一功能现在也内置于主流浏览器中。

不是不相关的，让我们加密即将[对他们的证书后台](https://letsencrypt.org/docs/certificate-compatibility/)进行更改。IdenTrust 证书允许 Let's Encrypt 最初起步，但足够的时间已经过去，足够多的设备现在信任 Let's Encrypt 根证书，因此不再需要 EdenTrust 证书。有一个列表列出了一些相当旧的硬件和软件，它们会因此而出现问题，请点击链接查看。

趋势科技的 [ServerProtect 产品已更新](https://success.trendmicro.com/solution/000289038)以修复其安全产品中的 0-click RCE。虽然不安全的安全产品并不新鲜，但这款产品尤其糟糕，CVSS 高达 9.8。