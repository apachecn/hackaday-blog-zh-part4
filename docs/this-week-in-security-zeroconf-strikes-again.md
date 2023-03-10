# 本周安全:Zeroconf 又来了，Lastpass 泄露了你最后的密码，你所有的数据都是我们的了

> 原文：<https://hackaday.com/2019/09/20/this-week-in-security-zeroconf-strikes-again/>

VoIP 摄像头、DVR 和其他运行网络服务动态发现(WSDD)协议的设备[正被用于一种新型的 DDoS 攻击](https://arstechnica.com/information-technology/2019/09/in-the-wild-ddoses-are-abusing-webcams-and-dvrs-to-amplify-their-crippling-effects/)。这不是 zeroconf 服务第一次被劫持为 DDoS 的一部分，因为 UPnP 也以类似的方式被滥用。

感觉像字母汤了吗？拒绝服务攻击只是让目标变得不可用，而不是真正受到威胁。这方面的经典例子是 SYN flood，在这种情况下，攻击者会同时打开数百个到 web 服务器的连接，耗尽服务器的资源并中断该服务器的合法使用。随着针对这些攻击的缓解措施的开发(例如， [SYN Cookies](https://en.wikipedia.org/wiki/SYN_cookies) )，DoS 攻击被分布式拒绝服务(DDOS)攻击所取代。DDoS 不是攻击目标机器上的弱点，如可用的 RAM 或 CPU 周期，而是通过一次从许多许多位置攻击目标网站来瞄准可用的网络带宽。当你的互联网连接被垃圾流量完全饱和时，再聪明的软件技巧也无济于事。

让许多许多计算机向同一个 IP 发送流量的一种方法是运行僵尸网络。你的 5 兆上传带宽可能看起来不多，但如果一千台计算机都饱和了它们的 5 兆，那么由此产生的 5 千兆攻击是不容忽视的。DDoS 扩大是指第三方服务被用作攻击的一部分。想象一下，发送一个带有假冒源 IP 地址的 DNS 请求。UDP 连接没有 TCP 数据包的初始握手，因此检测这种欺骗要困难得多。您发送一个相对较小的 DNS 请求，DNS 服务器通过发送一个较大的回复来响应—不是发送到您的 IP，而是发送到您假冒的目标 IP。这种放大通常是僵尸网络 DDoS 攻击的一部分，导致更多的攻击带宽。有记录以来最大的 DDoS 攻击是惊人的每秒 1.3 万亿字节，目标是 Github，并使用 Memcached 作为放大载体。

现在回到 Zeroconf。零配置网络是这样一种理念，即当一起接入网络时，事情应该“正常工作”。当您可以选择将视频发送到 Chromecast，或者 Windows 向您显示网络上所有其他设备的列表时，您会看到 zeroconf 在运行。像 UPnP 和 WSDD 这样的 Zeroconf 协议旨在仅在本地网络上运行，但是供应商因错误实施标准而臭名昭著，这里也不例外。根据定义，WSDD 应该只响应 UDP 端口 3702 上的多播请求。许多供应商已经以这样一种方式建立了他们的 WSDD 支持，即设备将响应来自任何 IP 地址的 WSDD 请求，无论是多播还是非多播。这种放大技术的最后一个关键是实际的放大。攻击者可以发送多小的数据包，而作为响应，它可以触发多大的数据包。Akamai 的研究人员发现了一条 18 字节的信息，它会引发更大的反应。他们获得了 153 倍的放大系数，这很可怕。幸运的是，主动攻击的放大倍数更接近 10 倍。

### 最后一遍显示你的最后一遍

有时软件名称和影响它们的 bug 是完全不可思议的。Lastpass 插件有一个问题，网站可以运行一些聪明的 Javascript，[检索 Lastpass 自动填充的最后一个密码](https://bugs.chromium.org/p/project-zero/issues/detail?id=1930)。这之所以有效，是因为 Lastpass 插件在你访问的网页上使用 Javascript，观察需要填写的密码提示。人们发现，恶意网站的 JS 代码可能会以意想不到的方式与插件的代码进行交互。因为可以在不调用初始化函数的情况下引用 Lastpass 弹出窗口，所以上次显示弹出窗口时的数据仍然存在。Lastpass 在 4.33.0 版中修复了该问题。

### 更多数据泄露

本周有两个关于大规模数据泄露的独立故事。尽管从技术上来说，没有密码的数据库被不小心暴露在互联网上也算不上是一个漏洞。首先是互联网上的 100 多个医疗数据库没有适当的安全保障。到目前为止，似乎有很多指责，但由于许多安全失败，有很多指责。值得注意的是，每一个暴露的数据库都违反了 HIPAA，并且都有可能被处以巨额罚款。

第二是厄瓜多尔几乎每个公民的记录。Elasticsearch 实例配置错误，可公开访问。虽然乍一看，这似乎是另一个暴露在互联网上的政府数据库，但这个数据库有些奇怪。有来自多个来源的数据。大约一半的数据库符合政府数据库的想法，但其余的似乎来自私人实体。研究这个故事的研究人员确定一家名为 Novaestrat 的厄瓜多尔公司托管着这个易受攻击的数据库。

数据库是安全的，诺瓦斯特拉特的网站已经消失了。关于这个故事，问题仍然多于答案。该数据库是其他数据泄露的组合存储吗？不管怎样，数百万厄瓜多尔人的个人数据被曝光。有趣的是，朱利安·阿桑奇是这个数据库中有条目的人之一，这是他在厄瓜多尔避难的结果。

这两个数据库都包含个人信息，这些信息当然是不可更改的。数以百万计的人因粗心大意而被欺骗，缺少证人保护计划级别的措施，没有撤销按钮。

### Windows Defender

使用 Windows Defender？下次手动运行扫描时，您可能会大吃一惊。自本周二更新以来， [Windows Defender 在手动运行快速或全面扫描时，仅扫描少量文件](https://www.bleepingcomputer.com/news/microsoft/windows-defender-antivirus-scans-broken-after-new-update/)。通常情况下，这个 bug 是在修复另一个问题时引入的。如果您使用 Windows Defender 并希望运行手动扫描，自定义扫描仍然可以正常工作。