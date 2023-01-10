# 本周安全:Adblock For Security、ProxyNotShell Lives 和 CVSS 10 To Not warm

> 原文：<https://hackaday.com/2022/12/30/this-week-in-security-adblock-for-security-proxynotshell-lives-and-cvss-10-to-not-worry-about/>

勒索软件仍然无处不在，这一次,[卫报宣布他们因受到攻击而部分关闭了](https://www.theguardian.com/media/2022/dec/21/guardian-hit-by-serious-it-incident-believed-to-be-ransomware-attack)。由于事故正在调查中，数据正在恢复，员工们正在家中工作。出版业似乎还在继续，印刷纸也如预期的那样运行。

最近发布了几份关于勒索软件和其他恶意软件如何传播的报告，第一份是来自联邦调查局的公共服务公告，详细说明了可能是盲目明显的攻击载体——搜索引擎广告。一个坏演员选择一个公司或常见的搜索词，支付搜索引擎的排名，然后建立一个看起来合法的虚假网站。对于加分，这使用了一个域名，如 adobe[dot]cm 或一个看起来更接近真实情况的 punycode 域名。

FBI 有三条建议，其中一条我完全同意。他们的第一个建议是在点击链接之前检查它们，这很好，除了 punycode 攻击。事实上，有足够多看起来相似的字形，使这基本上没有用。第二种是直接输入网址，而不是使用搜索引擎来查找公司的网站。这是伟大的，只要你知道网址，不要打错字。但老实说，我们这样做不都是意外地在网站[dot]co 结束了吗？他们最后的建议是好的，那就是运行一个高质量的广告拦截器来保证安全性。请记住，有选择地禁用阻止您想要支持的网站。(喜欢 Hackaday！)

## Exchange 仍然是目标

另一份报告，来自 Prodraft 的 PDF，详细描述了 FIN7 的活动，fin 7 已经将勒索软件添加到他们的犯罪组合中。这些攻击通过多种方式发起，包括恶意 USB 驱动器和使用已知的 Exchange 漏洞，如 CVE-2020-0688 和 ProxyShell 系列问题。

说到这里，ProxyShell/ProxyNotShell 并没有死，因为[在野外发现了另一个旁路](https://www.crowdstrike.com/blog/owassrf-exploit-analysis-and-recommendations/)。这不是对 11 月 8 日补丁的有效绕过，但确实绕过了被吹捧为有效缓解的重写规则。原因是这种攻击不使用自动发现端点，而是对 OWA (Outlook Web App)端点应用相同的技术。

## 密码管理器失败

LastPass 并不是新闻中唯一的密码管理器，在 Passwordstate 中发现的问题使得最近的 LastPass 问题看起来是最轻微的不便。Passwordstate 是一个用于密码管理的企业解决方案。modzero 的研究人员从浏览器扩展开始，允许用户访问保存的密码。为了进行身份验证，会生成一个令牌并发送给服务器。原来，这个令牌只是用户名和其他用户信息，与一个静态的通用密钥进行异或运算。在服务器端，唯一发生的检查是对用户名的检查。因此，在任何地方的任何 Passwordstate 安装上，如果您可以与 API 对话，并且知道一个有效的用户名，您可以获取该帐户的每个密码。

同样的 API 还有另一个问题，任何用户都可以写入任何其他用户存储的密码，包括给定密码的登录 URL。由于整个界面是基于 web 的，所以跨站点脚本攻击是必然的。当然，卫生工作做得不够。管理员可以使用 API 运行 Powershell 脚本。所以把恶意链接喷到其他用户的网址上，等着某个管理员用这个界面登录某个地方。powershell 脚本运行，启动一个反向 shell。因为存储的密码没有被有效地加密(AES 加密，但是密钥被存储、混淆在与数据库相同的机器上)，这允许攻击者带着整个密码数据库潜逃。在 9.6 版 Build 9653 中修复了这些漏洞，尽管看到问题和其他问题的严重性，人们不得不怀疑这些问题的处理效果如何。

## Linux 跳桑巴跳得很差

Linux 内核中有一个完美的漏洞。 [CVE-2022-47939](https://www.zerodayinitiative.com/advisories/ZDI-22-1690/) 是`ksmbd`驱动程序中的一个问题，它是去年为了更快的 SMB 性能而添加的。这里的 SMB 指的是服务器消息块，是 Windows 机器的主要文件共享协议。问题是一个悬空指针，允许释放后使用。解决方案是[一个单行补丁](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/?id=cf6531d98190fa2cf92a6d8bbc8af0a4740a223c)，它在关闭时将指针设置为空。

现在，尽管严重程度为 10 分的 CVE 病毒看起来很可怕，但我非常确定您没有什么可担心的，即使您是 Linux 用户或管理 Linux 服务器。为什么？因为虽然`ksmbd`在内核中是官方的*，但是几乎没有任何发行版将它编译到他们的官方内核中，Samba 项目没有使用任何易受攻击的代码，并且将任何 SMB 服务暴露给不受信任的连接已经是一个可怕的想法。或者换句话说，如果你在使用`ksmbd`驱动，你是故意的。*

 *内核配置选项是`CONFIG_SMB_SERVER`，你可以在`/proc/config.gz`或者`/boot/config-$(uname -r)`中检查你当前的配置。或者，使用`lsmod`搜索`ksmbd`模块。这可能是一个真正问题的真正地方是在运行 Linux 的 NAS 设备中，尽管我猜测内核模块是足够新的，以至于市场上流行的设备都没有使用它。如果您知道默认情况下编译该模块的主要发行版，或者使用它的 NAS，请务必让我们知道。

## 谷歌主页收购

谷歌的智能家居设备基于与 Chromecast 相同的固件，并使用类似的身份验证方法。 [[Matt]注意到了这一点，并开始思考](https://downrightnifty.me/blog/2022/12/26/hacking-google-home.html)，这会是一个安全问题吗？看，在电视上播放视频并不十分危险，但是一个聪明的扬声器有一些更重要的能力。Chromecasts 在本地 API 上提供一个密钥，向谷歌发送一个关闭该密钥的请求会将设备链接到你的帐户。其目的是本地网络上的任何人都应该能够在电视上播放。这个过程在其他智能设备上运行似乎是无意的。

但是等等，还有更多。这些设备具有设置模式，在该模式下，它们广播开放的 WiFi 网络。触发这种模式所需要的只是让设备离线——这就像发送伪造的 deauth 无线数据包一样简单。连接到网络，发出 API 请求，您就有了密钥。让它重新连接到真实的网络，你可以作为一个新的验证用户进行身份验证。智能家居行动让你可以用其他设备做一些有趣的事情，但仅仅是从设备上安静地打电话的能力就足够令人毛骨悚然了。谷歌同意了，并删除了非预期的授权流和通过例行程序拨打电话号码的功能。

## 比特和字节

TYPO3 内容管理系统[在本月早些时候修复并宣布了 RCE](https://typo3.org/security/advisory/typo3-core-sa-2022-015)。这个只有通过验证的用户才能访问表单设计器模块，但是允许注入可以作为 PHP 代码执行的输入脚本。

不要相信[从互联网上保存游戏](https://github.com/swoops/video-game-save-file-trojans/)。这是一个很好的一般性建议，但特别适用于基于 Ren'Py 的游戏，这是一个基于 Python 的视觉小说引擎。为了加载保存游戏，使用了 pickles 库——它已经因为在解压不可信数据时不安全而臭名昭著。只是不太明显的是，保存游戏可以通过 Python 函数反序列化自己并接管程序执行。

Netgear RAX30(可能还有其他型号)在启动时运行`pucfu`应用程序，检查 Netgear 域中的固件更新。[NCC 集团的研究人员发现](https://research.nccgroup.com/2022/12/22/puckungfu-a-netgear-wan-command-injection/)如果他们控制 JSON 对该请求的响应，二进制文件可以被操纵成命令注入，导致反向外壳。*