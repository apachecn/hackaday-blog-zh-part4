# 本周安全:Ubiquiti、日产、Zyxel 和 Dovecot

> 原文：<https://hackaday.com/2021/01/15/this-week-in-security-ubiquiti-nissan-zyxel-and-dovecot/>

你可能是本周收到来自 Ubiquiti 的电子邮件，建议修改密码的许多人之一。这封邮件称，Ubiquiti 系统存在未经授权的访问，虽然没有用户数据被访问的证据，但也没有足够的证据强调用户数据没有被访问。Ubiquiti 提到，可能被访问的数据库包含用户名、电子邮件地址、散列密码，以及可选的邮寄地址和电话号码。

根据 Ubiquiti 认证系统的设计，散列密码可能足以登录某人的帐户。在任何情况下，更新您的密码都会使潜在的受损哈希无效。这一事件凸显了 Ubiquiti 用户的抱怨:Ubiquiti 一直在让没有启用云的帐户的硬件管理变得困难。

### 日产源代码

日产使用 Atlassian 的 Bitbucket 托管了一个大型 git 存储库。那个安装仍然使用管理员帐户的默认凭证[，有人终于注意到了](https://www.zdnet.com/article/nissan-source-code-leaked-online-after-git-repo-misconfiguration/)。最先发现这个问题的研究人员一直保持匿名，而相关文章的主要来源[在最近爆发的 Twitter 审查中陷入困境，一个账户被暂停。](https://twitter.com/antiproprietary)

该存储库包含来自日产移动应用程序的代码、营销信息和仅供内部使用的服务代码。18.4 GB 的数据转储仍然可以通过 torrent 文件在互联网的黑暗角落使用。

### ISC 看到的 Zyxel 扫描

还记得我们上周谈到的 Zyxel 问题吗？这没花多长时间。互联网风暴中心(ISC)报告称[已经发现使用这些硬编码凭证的 SSH 登录尝试](https://isc.sans.edu/diary/rss/26954)。

值得花一分钟的时间来呼吁 ISC 和类似的努力，为他们的宝贵工作。ISC 主要作为入侵检测系统和防火墙的数据交换中心。当新的模式出现时，观察数据的志愿者可以快速识别新出现的攻击。在某些情况下，这种快速响应可以让世界各地的管理员有时间在漏洞受到危害之前修补目标漏洞。

### 鸽巢冬眠

Dovecot 已经发布了[版本 2.3.13](https://dovecot.org/pipermail/dovecot-news/2021-January/000448.html) ，并且有一个针对显著漏洞 [CVE-2020-24386](https://dovecot.org/pipermail/dovecot-news/2021-January/000450.html) 的修复。IMAP 支持 IDLE 命令，将与服务器的连接置于保持模式，准备将实时邮件通知推送到客户机。该漏洞允许客户端将其连接置于这种状态，然后向服务器发送恶意请求。该请求允许有限的文件系统访问，尤其是从其他帐户下载邮件。可以通过禁用 IMAP 休眠来缓解这一缺陷，但建议升级到最新版本。

### 电报三角测量

电报是发送安全信息的首选解决方案之一。就在一年多前，Telegram 推出了“我附近的人”(People Near Me)，这是一项查找附近选择使用该服务的用户的功能。如果你已经决定加入，你可以考虑关闭这个功能。Telegram 给任何在 7 英里内的人一个非常精确的距离。这个距离是实时更新的，这对聚会来说很好。可能不会立即显而易见的是，将设备的位置欺骗到世界上的任何地方都是相当微不足道的。几分钟之内，[就有可能精确定位世界上任何一个开启了【Telegram 定位服务的人。其他服务通过提供不太精确的位置数据来防止这个问题。到目前为止，Telegram 回应称这不是 bug，也不打算做任何改动。](https://www.androidpolice.com/2021/01/05/telegrams-people-nearby-feature-reveals-exact-user-locations-through-triangulation/)

### 太阳风是如何被黑的

太阳风借壳的更多细节正慢慢浮出水面。透露的信息越多，故事就变得越有趣。本周，我们得到了 Crowdstrike 对运行在 Solarwinds 机器上的恶意软件的报道。这个被称为黑子的恶意软件并不是 Orion 后门本身，它是一个定制的恶意软件，在编译时偷偷修改源代码。这让我想起了古老的[信任信任](https://www.cs.cmu.edu/~rdriley/487/papers/Thompson_1984_ReflectionsonTrustingTrust.pdf)攻击。

黑子被写得非常小心地隐藏起来，只有当它检测到代码编译时才采取行动。它每秒检查一次`MsBuild.exe`，以及它是否正在建造猎户座。如果是，它会修改一个源代码文件，等待编译完成，然后撤销恶意更改。开发人员很难发现这种修改，因为它只存在于编译期间，而开发人员无论如何都要出去喝咖啡。当 Solarwinds 第一次称之为“复杂而新颖”的黑客时，我们有些怀疑，但证据似乎证实了这一观点。