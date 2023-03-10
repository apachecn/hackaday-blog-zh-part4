# 本周安全:交换零日，二重身，Python 被咬在焦油中

> 原文：<https://hackaday.com/2022/09/30/this-week-in-security-exchange-0-day-doppelgangers-and-python-gets-bit-in-the-tar/>

据 GTSC 的研究人员称，[有一种未打补丁的 0-day 被广泛用于利用完全打补丁的微软 Exchange 服务器](https://gteltsc.vn/blog/warning-new-attack-campaign-utilized-a-new-0day-rce-vulnerability-on-microsoft-exchange-server-12715.html)。当他们发现一台服务器遭到破坏时，他们通过 ZDI 向微软报告，但当发现多台 Exchange 服务器遭到破坏时，他们向所有人发出了警报。看起来这是一种类似于 [ProxyShell](https://www.mandiant.com/resources/blog/pst-want-shell-proxyshell-exploiting-microsoft-exchange-servers) 的攻击，因为它使用自动发现端点作为起点。根据在安装的 webshell 中发现的一些迹象，他们怀疑是一个中国团体在利用这一漏洞。

有一个临时缓解措施，在字符串`.*autodiscover\.json.*\@.*Powershell.`上添加一个基于 URL 的请求块。确切的细节可以在帖子里找到。如果您使用 IIS 运行 Exchange，现在应该会将它添加到您的系统中。接下来，使用[自动化工具](https://github.com/ncsgroupvn/NCSE0Scanner)，或者运行 PowerShell 一行程序来检测危害:`Get-ChildItem -Recurse -Path -Filter "*.log" | Select-String -Pattern 'powershell.*autodiscover\.json.*\@.*200`。这一个有可能成为另一个真正令人讨厌的问题，并且可能被蠕虫感染。截至撰写本文时，这是 Microsoft Exchange 中一个突出的、未打补丁的问题。在保护好您的系统之后，请回来完成本文的剩余部分。

## Digital Dopplegangers

几周前，[Connor Tumbleson]收到了另一位开发人员[Andrew]，[发来的一封电子邮件，他被雇来假扮[Connor]参加工作面试](https://connortumbleson.com/2022/09/19/someone-is-pretending-to-be-me/)。说什么？这个骗局对我们来说是一个新的骗局，似乎是这样的:骗子选择了一个有专业图片和令人印象深刻的活动的 GitHub 帐户，然后以高级开发人员的名义创建了一个 Upwork 帐户。这包括对目标开发者的公开可用数据的深入研究。接下来，我们的骗子联系了另一个 GitHub 帐户持有人，他的资历不太好——一名初级开发人员，并提出了一份工作邀请:与一个不会说英语的开发团队合作，做一些开发工作，并在与北美客户合作时作为团队的代言人。这项工作唯一不确定的地方是，新员工会以队友的名义进行面试。

[![](img/adc9802531a19f2d2ea7c8e8a1d34493.png)](https://hackaday.com/wp-content/uploads/2022/09/emailing-myself.png)

这就把我们带到了[Andrew]，他是这个场景中的“初级开发人员”。这一切似乎都是合理的，直到他意识到他应该代表的团队成员实际上不是团队的一部分，并联系到真正的[康纳]，他开始挖掘。

这归结为一个雇佣骗局，试图使用一个熟练的开发人员的名字和声誉来获得合同。留意 Upwork 或类似招聘网站上的虚假简介。如果你得到了一个听起来和咬了安德鲁一口的报价相似的报价，那就要小心了。最后，如果你通过 Upwork 雇佣了一个开发人员，也许要考虑一下你是否真的确认了你的新开发人员就是他们声称的那个人。

## 在 TAR 中改变时间字节 Python

对于这个 bug，我们现在要做的是回到过去，回到过去。CVE-2001-1267 是最初的`tar`目录遍历漏洞。您可以将`../`作为文件路径的一部分包含在 tarballs 中，并且`tar`会很乐意跟随目录路径指向的任何地方。想覆盖`/etc/passwd`？没问题。GNU 的开发者意识到这是一个漏洞，并在 1.13.20 版本中修复了 GNU。快进到 2007 年，[【简·马特杰克】注意到 Python 的 tar 解包器也有同样的问题](https://mail.python.org/pipermail/python-dev/2007-August/074290.html)。经过一番讨论后，这个问题被[确定为 notabug，并以文档更新](https://github.com/python/cpython/issues/45385#issuecomment-1093394689)结束。[这个问题在 2017 年](https://github.com/python/cpython/issues/73974)被再次提出，但从未付诸行动。

现在，我们来看看特雷克斯的最新发现。那里的研究人员首先认为他们在 Python 中发现了一个 0-day，然后才意识到这是一个很好的老 CVE-2007-4559，仍然潜伏着。尽管这种危险已被记录在案，但一些 Python 开发人员是否通过不安全地使用 Python tarfile 模块而错误地将易受攻击的代码引入了他们的项目？在 GitHub 上，搜索`"Import tarfile" language:Python`返回 30 万次点击。检查这些项目的子集[返回了 61%的漏洞率](https://www.trellix.com/en-us/about/newsroom/stories/research/open-source-intelligence.html)。呀！

## 铬根

谷歌 Chrome 正在做一些有潜在争议的新东西，这可能会打破常规，所以又是一个星期五。不过，这个有点特别。谷歌 Chrome 将开始推出自己的根商店。这基本上是浏览器认为有效的 HTTPS 证书的主列表。这里最大的优势是这意味着 Chrome 将在所有平台上表现相同，不再依赖于操作系统提供的证书列表。当然，这也意味着谷歌控制着谁可以使用 HTTPS。如果有一个证书是在操作系统端手动添加的，Chrome 将会获取它，并且也支持它。我们走着瞧。

## 间歇加密和其他字节大小的故事

勒索病毒活动有一个新的锦囊妙计——[间歇加密](https://www.sentinelone.com/labs/crimeware-trends-ransomware-developers-turn-to-intermittent-encryption-to-evade-detection/)。这是一种观察，即并非目标文件中的每个字节都需要加密，以使其对所有者不可用。每隔 16 个字节加密有助于更快的加密和更慢的检测。Sentinel One 还发现了其他趋势，如 Rust and Go 中编写的勒索软件，以及勒索软件即服务的更多变体。

WhatsApp [刚刚发布了 iOS 和 Android](https://www.whatsapp.com/security/advisories/2022/) 的更新，修复了一对远程代码执行漏洞，这两个漏洞都与视频处理有关。在一种情况下，它是一个可以通过实时视频调用到达的整数溢出，另一种情况是在处理视频文件时的整数下溢。

Twitter 有一个非常糟糕的问题，密码重置[实际上并没有使应用令牌](https://privacy.twitter.com/en/blog/2022/an-issue-impacting-password-resets)失效。因此，如果有人接管了一个帐户并登录了移动应用程序，更改密码并不会终止访问。问题已修复，受影响的任何人都已得到通知。

惠普[已经为他们的许多打印机](https://support.hp.com/us-en/document/ish_6839789-6839813-16/hpsbpi03810)发布了固件更新，修复了一对可以在他们的许多网络打印机上启用 RCE 的漏洞。关于这个问题没有太多可用的信息，但是一个攻击者在一个经常被忽视的设备中持续访问网络就足够可怕了。只需等待不可避免的驱动程序漏洞浪潮，恶意打印机可以在试图打印的机器上触发任意代码执行。