# 本周安全:Twilio，PongoTV 和 BootHole

> 原文：<https://hackaday.com/2020/07/31/this-week-in-security-twilio-pogotv-and-boothole/>

几周前，电信云提供商 Twilio 遭遇了令人尴尬的安全失败。问题是 Twilio 用来存放面向公众的内容的亚马逊 S3 桶。存储桶配置为公共读写访问。任何人都可以使用亚马逊 S3 API 对存储在那里的文件进行修改。

有问题的文件受 Cloudflare 的 CDN 保护，但 Cloudflare 的服务有一个问题。如果你知道 Cloudflare 背后的服务细节，往往可以直接与之交互。在许多情况下，知道受保护服务器的 IP 地址就足以完全绕过 Cloudflare。在这种情况下，CDN 背后的服务是亚马逊的 S3。对那里的文件所做的任何更改都会被 CDN 拾取。

有人发现了不安全的 bucket，并修改了作为 Twilio JS SDK 的一部分分发的 Javascript 文件。这种修改最初被描述为“非恶意的”，但在官方事件报告中，Twilio 声明注入的代码是正在进行的针对错误配置的 S3 桶的 magecart 活动的一部分。


### intelligent personal television 智能个人电视

本周，我们在黑客日热线上收到了一篇关于瑞典 IPTV 服务彭哥 IPTV 的报道。这份报告未经证实，但似乎有事发生。至少，pongotv.com 目前正在返回一个 Cloudflare 错误，“这个网站正在使用一个安全服务来保护自己免受在线攻击。”

![](img/2dd623fb9bc0ea91827929c208b19c70.png)

一对 Youtube [视频](https://www.youtube.com/watch?v=Kuep5wssBjY)似乎显示了对 Pongotv 后端的访问，以及暴露的客户记录等。在这一点上，我必须强调，这是未经证实的报告。根据所提供的细节，听起来情报提供者实际上非常密切地参与了这个故事，甚至可能是攻击背后的组织的一部分。

### Espressif

[Lukas Bachschwell] [在 Espressif SDK](https://lbsfilm.at/blog/wpa2-authenticationmode-downgrade-in-espressif-microprocessors) 中发现了一个缺陷，被追踪为 CVE-2020-12638。该漏洞会影响运行使用易受攻击的 SDK 构建的固件的设备。简而言之，它允许 WiFi 身份验证降级攻击。攻击者可以注入 WiFi 流量，并使设备在攻击者的控制下连接到网络。对于用于家庭自动化和其他类似应用的设备，这可能会产生严重的后果。SDK 涵盖的大多数设备都有补丁，其余的正在开发中。

### D-Link 贴片停产设备

作为对 Loginsoft 研究人员发现的一系列缺陷的回应， [D-Link 发布了一款生命周期结束的设备](https://supportannouncement.us.dlink.com/announcement/publication.aspx?name=SAP10169)的固件，并强烈建议停止使用其他受影响的设备。有问题的设备是 DAP-1520、DAP-1522 和 DIR-816L。

这些也不是复杂的漏洞。第一个， [CVE-2020-15892](https://research.loginsoft.com/vulnerability/classic-stack-based-buffer-overflow-in-dlink-firmware-dap-1520/) ，只要在尝试登录时发送 256 个字符作为密码就可以触发。登录页面将该值限制为 15 个字符，但是该限制是强加在客户端的，因此攻击者可以轻松地操纵原始响应来绕过该限制。比预期长的密码溢出缓冲区，使设备崩溃。一个合适的漏洞会取而代之。

另一个相当小的漏洞， [CVE-2020-15893](https://research.loginsoft.com/vulnerability/multiple-vulnerabilities-discovered-in-the-d-link-firmware-dir-816l/) ，影响了 DIR-816L。可以在 UPnP 请求中插入 shell 命令，就像在数据包数据中包含分号一样简单。当 UPnP 请求被解析时，它的一部分被用作命令行选项。包含分号会中断该命令，并允许执行任意命令。

### Sharepoint

CVE-2020-1147 是微软 Sharepoint 中的一个漏洞，由多名研究人员独立发现。Source Insight [的【史蒂文】写了一篇关于 bug](https://srcincite.io/blog/2020/07/20/sharepoint-and-pwn-remote-code-execution-against-sharepoint-server-abusing-dataset.html) 的解释，并得出结论，其核心是一个反序列化问题。在这种情况下，数据集对象的函数，如`parse()`和`Deserialize()`可能会被反序列化的数据覆盖。

这篇文章包括一个完整的概念验证，所以请考虑这个已经完全武器化的漏洞。补丁是可用的，所以一定要照顾好你的 Sharepoint 服务器。[Steven]还暗示我们会在其他地方看到同样的错误。net 应用程序，因为数据集对象被认为对外部数据是安全的。

### 苹果研究设备

[![](img/e7cc72bc1e0b0c938dd26bdaa8ac9ef3.png)](https://twitter.com/benhawkes/status/1286021329246801921) 苹果公司宣布[安全研究设备](https://developer.apple.com/programs/security-research-device/)，这是一款本质上源于工厂的改良版 iPhone。该程序以典型的苹果方式运行，因为该设备一次只能借出 12 个月，并附有一份“该做什么”和“不该做什么”的清单。我不得不怀疑这是否是对去年谷歌 Project Zero 的可调试 iPhone 作品的回应。不管怎样，Project Zero 的本·霍克斯(Ben Hawkes)已经发表声明，该项目对他们来说很可能不会启动，因为他们严格的 90 天披露政策与签约协议不相容。

### 靴孔

最后，[grub 2 中的一个漏洞本周发布，BootHole](https://eclypsium.com/2020/07/29/theres-a-hole-in-the-boot/) 。该漏洞是一个相当简单的缓冲区溢出错误，可由恶意的`grub.cfg`文件触发。你可能会指出，如果攻击者可以修改`grub.cfg`，系统不就无可救药地被攻破了吗？这是一个公平的问题，答案通常是肯定的。BootHole 的新颖之处在于，以这种方式控制 Grub 可以允许安全引导绕过。在安全引导是安全性的关键部分的特定用例中，这显然更重要。

这个漏洞是由[eclypsium]发现的，他私下向 Grub 开发者和其他上游项目披露了这个 bug。补丁是可用的，所以请确保安装这些更新。如果你对深入的细节感兴趣，BootHole 上的文章和 [PDF](https://eclypsium.com/wp-content/uploads/2020/07/Theres-a-Hole-in-the-Boot.pdf) 相当详细，去看看吧。