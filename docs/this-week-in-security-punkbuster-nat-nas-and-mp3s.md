# 本周安全:PunkBuster、NAT、NAS 和 MP3

> 原文：<https://hackaday.com/2020/10/02/this-week-in-security-punkbuster-nat-nas-and-mp3s/>

啊，无处不在的 PDF，以及我们对这种格式的爱恨情仇。我们已经数不清 PDF 软件中有多少漏洞被修复了，但这些年来已经有很多了。本周，我们注意到 Adobe 并不是 PDF-land 的唯一玩家，因为 [Foxit 发布了一轮更新](https://www.foxitsoftware.com/support/security-bulletins.html)，并且修复了几个严重的问题。在这些漏洞中，有几个会导致 RCE，所以如果你使用或支持 Foxit 用户，一定要更新它们。

### 庞克巴斯特

记得 PunkBuster 吗？这是最早的反作弊解决方案之一，可以追溯到 2000 年。现在经典的《重返沃尔芬斯坦城堡》是第一款支持 PunkBuster 防止作弊的游戏。它不是最新或最棒的，但 PunkBuster 即使在今天仍在一堆游戏服务器上运行。[Daniel Prizmant]和[Mauricio Sandt]决定在 PunkBuster 上做一个深入的项目，而[碰巧发现了一个任意文件写入漏洞](https://medium.com/@prizmant/hacking-punkbuster-e22e6cf2f36e)，它可以轻松地危及启用 PB 的服务器。

PunkBuster 的功能之一是远程截图。如果服务器管理员认为某个玩家行为异常，就会发送截图请求。我认为这是针对所谓的 wallhack 欺骗——使纹理透明，这样玩家就可以看穿墙壁。问题是处理传入图像的服务器逻辑有一个漏洞。如果文件名如预期的那样以`.png`结尾，一些遍历攻击检查就完成了，png 文件被保存到服务器。但是，如果传入的文件不是 png，则不会进行横向检测，文件会被简单地写入磁盘。这一弱点，加上屏幕截图请求的无状态特性，意味着任何连接的客户端都可以在任何时间将任何文件写入服务器上的任何位置。值得称赞的是，PunkBuster 的创建者 even Balance 很快承认了这个问题，并发布了一个更新来修复它。

### NAS 勒索软件

[QNAP 宣布了一项更新，以抵御 AgeLocker 勒索软件](https://www.qnap.com/de-de/security-advisory/qsa-20-06)。详细信息很少，但似乎照片站应用程序中存在漏洞。[哔哔声电脑有一些额外的细节](https://www.bleepingcomputer.com/news/security/agelocker-ransomware-targets-qnap-nas-devices-steals-data/)。尽管加密具有破坏性，但至少有一份报告也包括数据失窃。AgeLocker 也会影响 Linux 和 MacOS 设备。

### MP3Gain 的损失

VDA 实验室的好人们对 fuzzing 情有独钟，最近，[他们将注意力转向了 MP3Gain](https://vdalabs.com/2020/09/03/vda-uses-mayhem-to-fix-mp3s/) ，一个开源的 MP3 标准化器。使用 [Mayhem](https://forallsecure.com/) 引擎，他们发现了一些崩溃，并发现了一个可能导致代码执行的崩溃。崩溃是由于格式错误的 mp3 文件，以及加载文件时没有足够的验证。

虽然 MP3Gain 可能不是最有可能的攻击媒介，但不难想象它可能被使用的场景。据我所知，还没有针对这个问题的更新版本。有足够的信息表明，攻击者可能会构建一个工作漏洞，所以如果您使用 MP3Gain，请格外小心，直到更新可用。

### 穿过 NAT 针

网络地址转换(NAT)是福是祸。它给了我们几年的时间来喘息 IPv4，并设法给每个人一个健全的防火墙默认设置。另一方面，点对点连接和 UDP 数据包很难通过 NAT 路由器。这是 torrents、SIP 电话呼叫以及 OpenVPN 和 Wireguard 等 VPN 解决方案的问题。多年来已经有了各种各样的解决方案，比如用于 SIP 的 STUN 服务器，以及用于自动执行临时端口转发的 UPnP。

Tailscale 是一家使用 Wireguard 提供网状 VPN 服务的商业公司，他们最近发布了一份关于他们穿越 NAT 防火墙技术的深度指南。这几乎是你想知道的关于这个主题的全部内容，所以读一读吧，或者只是在心里记下它，以便下次你发现自己面临棘手的 NAT 防火墙问题时使用。