# 本周安全:防火墙 0-day，苹果的反应，和一个 Android 蓝牙 Bug

> 原文：<https://hackaday.com/2020/05/01/this-week-in-security-firewall-0-day-apples-response-and-an-android-bluetooth-bug/>

Sophos 防火墙设备[正受到来自 SQL 注入的 0 天攻击链](https://news.sophos.com/en-us/2020/04/26/asnarok/)的攻击。这种注入是令人讨厌的，因为它可以从 WAN 用户门户启动。观察到的攻击者利用该漏洞向设备数据库中注入一个 shell 命令，该命令最终会自动运行。如果你有一个受影响的 Sophos 设备，去检查修复程序是自动安装的。

虽然这是一个糟糕的漏洞，Sophos 在这里的反应是值得称赞的。他们在接到攻击存在于野外的通知后不到 24 小时就公开披露了这一攻击，并开始在三天内推出修复程序。此外，Sophos 工程师做了一份非常详细的报告(链接如上),向我们提供了攻击的所有细节。修补程序关闭漏洞也试图清除感染，虽然有一些额外的手动步骤，建议如果您的设备受到损害。

注入的命令下载一个安装程序脚本，该脚本试图隐藏其感染媒介，下载一些二进制文件，然后在现有的系统脚本中添加一个持久挂钩。从那里，恶意软件似乎进入了观察模式，试图将关于主机设备的数据上传到命令和控制服务器。Sophos 表示，“我们没有发现任何证据表明所收集的数据被成功泄露。”他们在这个问题上的文章缺少的是他们得出没有客户数据被盗的结论的推理。

该攻击是由于恶意软件代码中的一个 bug 而被发现的。隐藏感染的尝试就像删除恶意的 SQL 数据一样简单，但在某些情况下，合法的条目显然会被删除，而注入的代码会显示在管理员仪表板上。虽然不确定攻击持续了多长时间，但与此次活动相关的 DNS 名称似乎都是在今年 3 月下旬注册的。

### 从未发生的 iOS 攻击？

上周[我们讨论了一些特别可怕的 iOS 邮件漏洞](https://hackaday.com/2020/04/24/this-week-in-security-nintendo-accounts-pernicious-android-malware-and-an-ios-0-day/)。几天过去了，[苹果回应了](https://arstechnica.com/information-technology/2020/04/apple-disputes-report-of-non-click-ios-0day-under-exploit-for-two-years/)。他们承认这是一个新的 bug，但对它可能被用于设备妥协的想法提出了质疑，并坚持认为这些 bug 不太可能被实际用于攻击。

苹果的声明重申了 ZecOps 研究人员所说的一件事:这个 bug 不足以逃脱邮件系统上下文。这本身当然是真的。有趣的是，ZecOps 的研究人员是否能找到一个额外的漏洞，使系统受到损害。到目前为止，ZecOps 坚持认为这是一个野外漏洞。我们将继续关注这一有趣事件的更多进展。

> 苹果严肃对待所有关于安全威胁的报告。我们已经彻底调查了研究人员的报告，并根据所提供的信息得出结论，这些问题不会对我们的用户构成直接风险。研究人员在邮件中发现了三个问题，但仅凭这些不足以绕过 iPhone 和 iPad 的安全保护，我们也没有发现他们被用来对付客户的证据。这些潜在的问题将在不久的软件更新中得到解决。我们重视与安全研究人员的合作，以帮助保护我们用户的安全，并将感谢研究人员的帮助。

### SMB 中继攻击

针对微软 NTLM 认证方案的中继攻击已经是旧闻了。许多年前，人们发现针对 SMB 服务器的中间人攻击是进入组织网络的有效方法。用户认为他们正在用一台已知的机器进行身份验证，但实际上他们的身份验证会话是通过一个恶意的中介进行的。在近 20 年后，这个问题肯定已经被彻底解决了，对吗？通常情况下，向后兼容性会给这类协议漏洞带来比预期更长的寿命。

27 日，来自 SecureAuth 的研究人员发表了[一种让中继攻击更有效的新方法](https://www.secureauth.com/blog/what-old-new-again-relay-attack)。SMB 消息“状态 _ 网络 _ 会话 _ 过期”触发会话重新认证，无需用户交互。一旦用户通过 MitM 服务器建立了活动连接，攻击者就可以触发重新认证，并将新的认证反映到不同的服务器。这是一个聪明的攻击，他们甚至公布了[使其工作的代码](https://github.com/SecureAuthCorp/impacket/commit/a0aca12c29d5ce80373ea6b83f9d774089b226bb)，所以如果 SMB 攻击是你的事情，去看看吧。

### 死亡 GIF

不，不是什么看着一个女孩从井里爬出来的 GIF 的都市传说。这是子域劫持和让用户交出微软团队认证 cookie 的巧妙结合。

[![](img/5c27905a997d8f8ca517ba1de533f221.png)](https://www.cyberark.com/threat-research-blog/beware-of-the-gif-account-takeover-vulnerability-in-microsoft-teams/?wvideo=f4b25lcyzm) 第一，[子域劫持](https://www.hackerone.com/blog/Guide-Subdomain-Takeovers)。对于一个组织来说，拥有各种不活跃的子域并不罕见。这些域实际指向哪里？在某些情况下，他们指向类似 GitHub 页面的某个地方，但是没有设置帐户。如果别人认领了那个账号会怎么样？像`data-dev.teams.microsoft.com`这样的东西可能会突然被与微软无关的人控制。

一个`teams.microsoft.com`认证 cookie 和任何 HTTP 请求一起被发送到`teams.microsoft.com`或任何子域。那么如何让某人访问被陷的子域呢？这就是 GIF 出现的原因。通过团队发送 GIF 链接会自动从恶意子域加载 GIF，并随其一起发送 auth cookie。又是一场大火。

[小心微软团队的 GIF:账户接管漏洞| CyberArk](https://www.cyberark.com/threat-research-blog/beware-of-the-gif-account-takeover-vulnerability-in-microsoft-teams/?wvideo=f4b25lcyzm)

### 安卓蓝牙 Bug

除了进一步挑 iOS 的毛病，还有一个安卓的缺陷需要考虑。SEEMOO 实验室的[Jan Ruge]通过 fuzzing 发现了 Android 蓝牙堆栈中的一个奇怪的崩溃。通过跟踪崩溃，他们发现格式错误的蓝牙数据包片段可能会导致系统调用长度值为负的`memcpy`。由于数据类型`size_t`，这个负值在`memcpy`调用中被解释为一个非常大的正值。人们会认为这会将垃圾写入内存，直到到达可寻址内存的末尾，从而导致内核崩溃和重新启动。相反，由于`memcpy`中的优化，一些数据是从负内存偏移量复制的。在蓝牙 ping 请求的情况下，这可能会泄漏 ping 响应包中的内存内容。

如果前一个包恰好在内存中当前包的前面，就有可能覆盖实际的结构头，结果会泄漏更多的信息。到目前为止，这个 bug 听起来和 [Heartbleed](https://heartbleed.com/) 差不多。因为它是由攻击者控制的`memcpy`触发的，所以有更多的可能性。事实上，研究人员确实找到了一个他们可以覆盖的指针，并最终将执行跳转到他们控制的内存中。这是一个复杂的过程，成功率不到 50%,但不妥协的崩溃只是崩溃和重启蓝牙守护程序，允许多次尝试。

这个漏洞被私下透露给谷歌，并在 2 月的安全更新中修复。没有任何证据表明这已经在野外被利用了，但是既然报告已经公开，确保你是最新的是很重要的。如果你想了解 SEEMOO 小组用来发现这个 bug 的工具的更多信息，[Jiska Classen]在 12 月份谈到了[实验室的蓝牙工作](https://hackaday.com/2019/12/30/36c3-all-wireless-stacks-are-broken/)，她刚刚详细介绍了我们仍在关注的弗兰肯斯坦工具。