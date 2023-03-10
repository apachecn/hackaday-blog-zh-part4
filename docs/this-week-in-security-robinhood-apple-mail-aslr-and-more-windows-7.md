# 本周安全:罗宾汉、苹果邮件、ASLR 和更多 Windows 7

> 原文：<https://hackaday.com/2020/02/14/this-week-in-security-robinhood-apple-mail-aslr-and-more-windows-7/>

本周首先，一个名为 Robinhood [的勒索软件有一个新奇的锦囊妙计](https://news.sophos.com/en-us/2020/02/06/living-off-another-land-ransomware-borrows-vulnerable-driver-to-remove-security-software/)。诀窍？加载旧的已知易受攻击的签名驱动程序，然后利用该驱动程序中的漏洞加载恶意内核驱动程序。

一个千兆字节的驱动程序无意中暴露了一个允许不受约束的内核级读写访问的接口。因为它是正确签名的，所以 Windows 会很乐意加载驱动程序。勒索软件代码使用该接口来关闭强制只加载签名驱动程序的位。从那里，加载一个恶意的驱动程序是微不足道的。在启动数据加密之前，Robinhood 使用其内核级访问权限来禁用防病毒应用程序。

这是二进制签名弱点的一个突出例子，没有撤销这些签名的机制。在理想情况下，一旦发现漏洞并发布更新，旧的、易受攻击的驱动程序的签名将被撤销。

### 这次可能是最后一次真正的 Windows 7 更新

关于 Windows 7/Server 2008 即将寿终正寝的更多新闻。KB4539602 周二发布了这个补丁，修复了上一轮“最终”更新中引入的黑色背景问题。这肯定是我们最后一次听到这个故事了，对吗？

没那么快。显然，这个补丁已经导致多台 Windows Server 2008 机器在安装了之后[无法启动。据微软称，问题是更新 SHA-2 支持的先前补丁丢失。](https://www.bleepingcomputer.com/news/microsoft/windows-server-2008-servers-don-t-boot-after-kb4539602-update/)

### 苹果邮件曝光加密邮件

早在 11 月份，[鲍勃·詹德勒]就发现了苹果邮件处理加密邮件的一些令人不安的地方。在 MacOS 上，suggestd 服务收集电子邮件和文件的片段，以更智能地处理搜索和 Siri 请求。[结果数据集包含电子邮件](https://medium.com/@boberito/apple-mail-stores-encrypted-emails-in-plain-text-database-fix-included-3c2369ce26d4)的明文，甚至包括那些使用 GPG 加密的邮件。他给出了一套解决方案，并通知了苹果公司这个问题。

就在最近，苹果推送了 10.15.3，在更改日志中埋下了一条说明，声明加密邮件将不再出现在 spotlight 搜索中。[【Bob】做了一些进一步的测试](https://medium.com/@boberito/apple-mail-encryption-bug-fixed-d10f7395352e)，并确认 suggestd 服务现在可以识别加密消息，并立即删除这些消息中的片段。

### Gitlab 的 GCP 深潜

对谷歌的云平台感到好奇，那里的安全考虑与更传统的环境有何不同？Gitlab 对 GCP 做了一些研究，它变成了探索和妥协 GCP 项目的分步指南。

这里有一堆关于 GCP 的基本信息，以及导致易受攻击实例的常见错误配置。这篇文章中我最喜欢的一句话是:遵循脚本。如果您找到一个备份脚本，您不仅可以使用一些凭证，还可以获得整个文件系统的副本。该指南包括转移到其他虚拟机的技巧，以及危及整个谷歌套件帐户的可能途径。

### Linux ASLR

地址空间布局随机化(ASLR)是 2005 年添加到 Linux 内核中的一项安全增强功能。它使用户空间程序的内存布局随机化，努力使实际的危害更难实现。例如，如果您有一个缓冲区溢出，当程序每次运行时内存布局都不同时，您如何编写一个漏洞？

Wildfire 实验室的人看了看 Linux ASLR 版本，得出的结论是仍然缺乏。主要问题是“/proc/[pid]/*”中可用的信息，以及对这些虚拟文件进行安全检查的方式。最直接的例子是“/proc/[pid]/maps”，它包含随机化的内存布局。正如 2019 年年中所披露的那样，当另一个应用程序试图读取其内容时，这个虚拟文件将进行权限检查，但当试图简单地打开文件时，则不会进行权限检查。实际上，这意味着非根应用程序可以获得指向“映射”虚拟文件的文件描述符，并将该描述符传递给另一个应用程序。如果传递给 setuid 根应用程序，受保护的信息可以被自由读取，并可能泄漏回无特权的应用程序。

“Setuid root”值得一提。Ping 是一个完美的例子:允许非根用户使用 ping 命令来测试网络连接是合理的。发送 ICMP 数据包需要一个原始套接字，这反过来又需要 root 权限。我们如何安全地允许非根用户访问该功能？Setuid 是可执行文件的一种特殊文件权限，允许可执行文件以 root 用户身份运行，而不管启动它的用户是谁。可以想象，要避免 setuid 二进制文件中的本地漏洞，需要非常小心。

虽然 maps 虚拟文件中的权限旁路问题得到了修复，但该修复并未应用于/proc 结构中的其余节点。Wildfire 工作的新颖性在于，他们发现了其他可以被类似滥用的节点，以检索映射信息。关于当前的缓解措施是否足够，似乎与内核开发人员有一些分歧，但随着概念证明的发布，肯定会很快得到解决。

### 数据收集

本周最后一则新闻是关于 Wacom 平板电脑驱动程序收集了太多数据。期待来自我们自己的 Kristina Panos 的一篇专门的文章，仔细看看这个故事，以及用来弄清楚到底发生了什么的技术。