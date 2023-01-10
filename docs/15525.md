# 本周安全:华为获得 Banhammer、Lastpass 和旧代码破解

> 原文：<https://hackaday.com/2022/12/02/this-week-in-security-huawei-gets-the-banhammer-lastpass-and-old-code-breaking/>

当我们许多人享受感恩节假期的时候，美国政府对华为和其他四家中国公司采取了严厉的措施。受打击最大的是华为和中兴，因为该禁令阻止任何新产品获得美国市场的批准。另外三家公司是大华和海康威视，它们生产视频监控设备，海能达生产无线电系统。[联邦通信委员会委员布伦丹·卡尔指出了该决定的严重性。](https://twitter.com/BrendanCarrFCC/status/1596223086768029707)

> 由于我们的订单，没有新的华为或中兴设备可以被批准。除非大华、海康威视或海能达向联邦通信委员会保证他们的设备不会被用于公共安全、政府设施安全和其他国家安全目的，否则任何新的大华、海康威视或海能达设备都不会获得批准。

甚至有可能以前批准的设备会被撤销授权。如果你真的想浏览这些原始的 FCC 文件，你可以从处获得。值得注意的是，两个截然相反的美国政府都在推动这项禁令。看看详细说明实际发现的机密报告肯定会很有趣。也许再过十年或二十年，我们可以提出信息自由法案的要求，并最终获得完整的故事。

## 重新折叠的模糊化

[0xacb]有一个有趣的新技术可以分享，[他称之为重新塌陷](https://0xacb.com/2022/11/21/recollapse/)。这都是关于在用户输入验证和清理中使用的正则表达式。Regex 很难真正正确，并且在不同的语言和库实现它的方式上充满了怪癖。一个简单的例子是包含“puny code”——非 ASCII Unicode 字符——的电子邮件地址。地址包含 unicode 是完全合法的，但是许多规范化方案将 Unicode 字符串压缩成最接近 ASCII 的形式。取`exámple.com`和`example.com`。如果 web 服务的某个部分将这些视为同一事物，而另一个后端服务认为它们是唯一的，那么这种不匹配可能会导致帐户被接管。在此输入您的电子邮件以接收密码重置链接。

这里的新东西是一个结构化的方法来模糊这些问题。[0xacb]建议标识“正则表达式轴心位置”，即字符串中可能出现意外或不一致的正则表达式匹配的位置。一个非常不同的例子是字符串结束符号`$`。开发人员可能会用它来指定一个给定的模式只有在它位于一个字符串的末尾时才应该被匹配。但是当字符串中嵌入了一个换行符时会发生什么呢？这取决于语言。呀！

REcollapse 现在是一个开源工具，可以很好地将模糊输入输入到自动化工具中。对着一个目标运行，观察不同的反应。找点够好的，还有利润！

## 智能手表钓鱼

Cybervelia 的团队发明了另一种刺击目标的方法。我们许多人都有智能手表，这些腕上佩戴的神奇产品最有用的功能之一是浏览短信或其他信息，而无需掏出手机。攻击者可以用蓝牙低能量天线欺骗附近的智能手表发送短信吗？经过一些逆向工程的工作，当然。有了正确的信息，如“需要帮助，2 楼”，目标可能会在没有检查手机和发现欺骗的情况下就开始移动。

## 实时恶意软件搜索

[![](img/84a163d48f42f28dfe30923651833c62.png)](https://hackaday.com/wp-content/uploads/2022/11/pypi-malware.png) 这个挺好玩的，正当[Phylum 的研究人员发现又一个恶意 PyPi 包活动](https://blog.phylum.io/disrupting-a-software-supply-chain-threat-actor-building-a-botnet)15 号回来了。他们的工具在活动的早期就提醒了他们，因为包正在上传，有效载荷仍在微调。那个有效载荷是在 Github 上开发的，所以只有一件事要做。

迷因和安全研究的结合是一件奇妙的事情。这些软件包被报告、删除，看起来这种特殊的恶意软件活动在真正开始之前就被消灭了。

这确实引出了 Phylum 的一个有趣的话题，关于他们在其他战役中发现的一些[可笑可怕的恶意软件尝试。恶意软件拒绝运行是有一定道理的，因为解密程序会检查确认字符串，并在被篡改时出错。](https://blog.phylum.io/malicious-open-source-package-authors-are-bad-and-should-feel-bad)

## 最后一次突破继续

Lastpass】更新了他们的安全事故报告，指出似乎有后续的数据访问。他们注意到“第三方云存储服务中的异常活动”，这通常指的是亚马逊的 AWS。这里的[故事似乎是存储服务的一个令牌](https://www.bleepingcomputer.com/news/security/lastpass-says-hackers-accessed-customer-data-in-new-breach/)在八月的妥协中被窃取，并且刚刚被用于更多的恶作剧。这确实提出了一些令人不安的问题，即 Lastpass 在多大程度上了解早期入侵中访问了哪些数据。也就是说，在事件发生后进行清理是一项复杂的任务，在行动中丢失一个 AWS 令牌太容易了。

## 另一个“合法的”商业间谍软件供应商

在“我们需要的”类别中，来自谷歌威胁分析小组的最新[报告将瓦里斯顿列为商业恶意软件游戏中之前未知的玩家。像 NSO 集团和其他人一样，Variston 似乎可以在多种设备和平台上访问 0-day 漏洞。](https://blog.google/threat-analysis-group/new-details-on-commercial-spyware-vendor-variston/)

Chrome bug 系统中公开了三份[bug 报告，每份都包含一个成熟的框架和一个严重 bug 的漏洞利用代码。这些都是已知的已修复的 bug，但是将这些线索拼凑在一起可以表明它们被一个供应商用作 0-days，可能是 Variston。对于“合法”的间谍软件作者来说，如非政府组织、国家安全局和其他人，一旦他们完成了利用漏洞的工作，或者假设一旦目标发现了漏洞，他们就会正确地报告漏洞，这并不罕见。](https://arstechnica.com/information-technology/2022/11/google-ties-spanish-it-firm-to-0-days-exploiting-chrome-defender-and-firefox/)

## 500 年后

加密中有一个概念，如果有足够的时间和技术创新，几乎任何加密方案在理论上都是可以破解的。作为一个例子，看看量子计算机的发展速度，以及一些经典密码的预测崩溃。从这一现实中溢出的哲学是，加密只需要足够强大，当技术和计算能力赶上时，受保护的秘密就完全过时了。这最终把我们带到了这个故事，查理五世皇帝从他的密码中获得了将近 500 年的时间。可能够强了。

事实证明，这个密码有一些聪明的元素，比如根本没有任何意义的多个符号，只是为了让它更难理解。真正的突破是找到了一份被粗略翻译过的密文。这足以最终弄清楚基本规则。那么最终被破译的中心字母里是什么呢？政治操纵，对暗杀的恐惧，以及散布假新闻以淡化挫折的阴谋。有些事情永远不会改变。

## 字体指纹

休息期间，Reddit 上的一个帖子引起了我们的注意，一名用户从他在英格兰的银行在线汇款到肯尼亚，以支付旅行费用。这是一笔合法的交易，但引发了他的银行的欺诈保护。在与欺诈部门的对话中，一个可能的欺诈标志让问题中的 Redditor 大吃一惊:您的计算机上安装了 TeamViewer。

现在等等。这有点令人不安，一个网站可以看到你的安装程序列表？不，不是直接的。没有列出应用程序的 web API，至少，自从 ActiveX 死亡以后没有。但是，有一个 API 可以列出已安装的字体。由于 Teamviewer 自带了字体，所以很容易检测到它是何时安装的。面对现实吧，远程控制的桌面是恶意活动的合理标志。所以现在你知道了，你的字体可能只是你的指纹。

## 比特和字节

Google Play 商店[已经退出了两个比较受欢迎的应用](https://arstechnica.com/information-technology/2022/11/google-boots-play-app-that-surreptitiously-sent-texts-to-developers-server/)，这两个应用正在偷窥用户的短信。数据收集是偶然的，真正的目的是利用受害者的手机号码在各种网络服务上建立假账户。需要一百个推特账号？租用 100 部受损手机，用这些号码激活流程。

需要通过剽窃检查吗？[就 rot13 换字体](https://medium.com/@doctoreww/beating-plagiarism-checkers-for-science-step-by-step-1e477795e261)！这是一个愚蠢的演示，但它确实有效。制作您自己的字体以更改字母映射，然后将反向映射应用于底层文本。对人眼来说，这是一样的，但对自动化工具来说，这是垃圾。保存为 PDF 格式，然后就可以开始了。虽然绕过抄袭过滤器是一个坏主意，但这可能有其他更积极的用途，比如绕过审查。

黑帽 2022 [视频可用](https://www.youtube.com/playlist?list=PLH15HpR5qRsVKcKwvIl-AzGfRqKyx--zq)，仅三个月后。这里有一些有趣的演示，如 Starlink hack，对真实世界恶意软件活动的分析，以及许多软件被入侵。尽情享受吧！

 [https://www.youtube.com/embed?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent&listType=playlist&list=PLH15HpR5qRsVKcKwvIl-AzGfRqKyx--zq](https://www.youtube.com/embed?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent&listType=playlist&list=PLH15HpR5qRsVKcKwvIl-AzGfRqKyx--zq)

