# 本周安全:GoDaddy，Tardigrade，Monox 和 BigSig

> 原文：<https://hackaday.com/2021/12/03/this-week-in-security-godaddy-tardigrade-monox-and-bigsig/>

感恩节假期后，我们有两周的新闻要报道，所以请等待一个超长的条目。首先出场的是 GoDaddy，[他从 9 月 6 日](https://techcrunch.com/2021/11/22/godaddy-breach-million-accounts/)开始遭遇违约。[根据 SEC 的文件](https://www.sec.gov/Archives/edgar/data/1609711/000160971121000122/gddyblogpostnov222021.htm)，他们在 11 月 17 日注意到了这个问题，并确定 WordPress 主机服务的供应系统存在未授权访问。对于那些在家跟踪的人来说，这是一个恶意演员可以访问的两个月零十一天。什么都妥协了？大约 120 万 GoDaddy WordPress 用户的电子邮件地址和客户号；初始的 WordPress 密码，**中清除**；SFTP 和数据库的密码，也在明码中；对于一些客户来说，他们的私有 SSL 密钥。

值得庆幸的是，GoDaddy 的系统似乎隔离得足够好，这一违规行为似乎没有导致进一步的广泛妥协。目前还不清楚为什么密码会在初始设置程序之后以明文形式存储。为了安全起见，如果你有一个由 GoDaddy 托管的 WordPress 实例，你应该非常仔细地检查它是否有泄露的迹象，并轮换相关的密码。SSL 密钥可能是最麻烦的，因为这将允许攻击者模拟域。考虑到攻击进入的时间长度，我不会对 GoDaddy 的更多基础设施实际上受到损害感到惊讶。

## 缓步动物——也许

就在一周前，[新闻报道了一场针对生物制造行业的新 APT 恶意软件活动](https://www.wired.com/story/tardigrade-malware-biomanufacturing/)。这种新的威胁带有“半心半意的勒索信”，具有适应性、隐蔽性，并表现出自主行动。来自 BioBright 的研究人员将缓步动物描述为根据环境动态地重新编译自己，从而不断改变签名。

如果这听起来有点喘不过气来，有点言过其实，你并不孤单。一位以[Infosec co scribe]为笔名发表文章的研究人员整理了一份对迟来的披露的谴责性评论。~~“合作者”在这里可能指的是在禁止一种潜在危险的鸦片制剂时禁止一种解毒剂的做法，似乎暗示该帖子旨在对一些粗略的 infosec 报告进行解毒剂处理。~~评论者指出，医生开处方，而不是禁止。“粪”是一个前缀，指粪便。我会让你自己去理解它的意思。

[Infosec]指出，迟来的披露没有显示出真正彻底工作的迹象，并指出报告的妥协指标(IoCs)是一个例子。那些网络 IOC 是:“Amazon Web Services (AWS)的随机批处理”、GoDaddy 和 Akamai。很难找到一个不经常与 AWS、GoDaddy 域名和 Akamai CDN 对话的网络。恶意软件二进制文件似乎是这项研究的基础，是一个已知工具 CobaltStrike 的样本。没有进一步的澄清和细节，缓步动物作为 APT 的整个故事似乎是不可靠的。现在下定论还为时过早。这可能真的是另一个 Stuxnet 级别的操作，或者它可能只是一个没有经验的响应团队在阴影中跳跃。

## 氧化硅和一个愚蠢的智能合同错误

智能合约正在慢慢改变世界，至少某些加密硬币爱好者是这样认为的。更容易证明的是，智能合约中的漏洞可以非常迅速地破坏分散金融(DeFi)应用程序。最新的例子是旨在使代币交易变得更容易的 DeFi MonoX。问题是，有可能用一个 MONO token 来交换它自己。借用一个编程术语，这导致了未定义的行为。这种代币被反复交易，每次交易它的价值都会上升。MONO 的价格最终被抬高到足够高，攻击者可以用多边形和以太坊的代币来代替他的代币。损失的总价值为 3100 万美元。当钱是代码的时候，钱就会有 bug。

## bigbig

大签名的简称，[[塔维斯·奥曼迪]将他的 NSS 漏洞命名为大签名](https://googleprojectzero.blogspot.com/2021/12/this-shouldnt-have-happened.html)。没有华而不实的标志，所以你想怎么做就怎么做。这是一个简单的错误——为最大的有效签名分配一个缓冲区，当处理一个更大的畸形签名时，它会直接写入缓冲区的末尾。CVE-2021-43527 很简单，也很容易利用。它是固定在 NSS 3.73，在 1 日发布。虽然这个漏洞不会影响 Firefox，但其他应用程序，如 Thunderbird、LibreOffice 和其他应用程序都使用了 NSS 库，因此可能容易受到攻击。

这个故事最有趣的方面是，这段代码自 2012 年以来一直存在漏洞。这不是那些臭名昭著的单一维护者项目之一，而是 Mozilla 的一部分，Mozilla 竭尽全力确保安全。NSS 库有很好的测试覆盖率，已经被模糊化，并且是 Mozilla bug bounty 计划的一部分。我不确定是谁创造了这个短语，但这肯定证明了“代码想要出错”。[Tavis]在研究一种模糊代码覆盖率的新方法时发现了这个 bug。他指出，现有代码测试策略中的一个主要失败是，NSS 的各个模块是单独测试的，而不是以端到端的方式。输入模块可能能够将传入的请求解析为上下文结构，但是对照项目的其余代码测试结果上下文是很重要的。

## 美国电话电报公司主办 EwDoor

似乎有一个针对 EdgeMarc 企业会话边界控制器的活跃的恶意软件活动。早在 2017 年就发现了一个漏洞，一个默认密码(设置为“默认”)[可以与隐藏的 web 端点](https://depthsecurity.com/blog/cve-2017-6079-blind-command-injection-in-edgewater-edgemarc-devices)一起使用，允许运行任意命令。当 [Netlab 360 发现一个新的僵尸网络接管这些设备](https://blog.netlab.360.com/warning-ewdoor-botnet-is-attacking-att-customers/)时，这段古老的历史突然又变得相关了。EwDoor 可用于 DDoS 攻击、数据窃取，并包含反向外壳。这是一个令人讨厌的小软件包，AT & T 公司很惭愧，因为它似乎未能修补他们为客户拥有和管理的硬件中的严重漏洞。

## 椭圆曲线是如何出错的

NCC 集团已经[对正确验证椭圆曲线加密的挑战](https://research.nccgroup.com/2021/11/18/an-illustrated-guide-to-elliptic-curve-cryptography-validation/)有了一个很好的入门。他们警告的招数很简单，就是发无效分，希望对方没注意到。另一个有趣的方法是发送一个位于无穷远处的点。这似乎相当于在 Diffie-Hellman 交换中选择零作为基础——它缩短了整个过程。整篇文章值得一读。

## 铁丝网金丝雀

Thinkst 为他们的 Canarytokens 服务提出了一个有趣的前提——在真正的设备上放置假凭证，并检测假凭证何时被使用。他们的产品组合中增加了 Wireguard 。他们没有尝试使用完整的 Wireguard 实现，而是重新实现了握手启动代码，将他们的迷你项目称为 WireGate。这是一个聪明的想法，他们已经[公布了来源。](https://github.com/thinkst/canarytokens/blob/master/wireguard.py)反过来看，如果有人愿意的话，Wireguard 启动包似乎也可以用作端口敲门令牌。

## Linux —检测持久性

你的 Linux 机器被入侵了？你知道该怎么做。拔下插头，交换驱动器，然后重新安装。但是……您在寻找什么，既要检测受损情况，又要调查受损磁盘？[Pepe Berba]已经发表了关于 Linux 机器持久性技术的系列文章的前两部分。[第一个条目](https://pberba.github.io/security/2021/11/22/linux-threat-hunting-for-persistence-sysmon-auditd-webshell/)作为介绍，然后讨论使用`sysmon`和`auditd`来检测可能的问题，比如 webshells。[第二部分介绍账户创建和操作](https://pberba.github.io/security/2021/11/23/linux-threat-hunting-for-persistence-account-creation-manipulation/)，并再次给出立即捕捉变化的提示。这看起来是一个写得很好的系列，充满了好的技巧，所以请继续关注它。