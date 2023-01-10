# 本周安全:VPN、补丁星期二和 Plundervault

> 原文：<https://hackaday.com/2019/12/13/this-week-in-security-vpns-patch-tuesday-and-plundervault/>

最近披露了 Unix 虚拟专用网[中的一个问题，攻击者可能会劫持 TCP 流，即使该流在 VPN 内部。这种攻击会影响 OpenVPN、Wireguard，甚至 IPSec VPNs。这怎么可能呢？Unix 系统支持各种不同的网络场景，配置错误经常会导致问题。在这里，发送到 VPNs IP 地址的数据包被处理和响应，即使它们通过不同的接口进入。](https://seclists.org/oss-sec/2019/q4/122)

这种攻击起初听起来难以置信，因为攻击者必须知道 VPN 客户端的虚拟 IP 地址、活动 TCP 连接的远程 IP 地址以及该连接的序列号和 ack 号。这是大量的信息，但攻击者可以一次找出一部分，使其成为一种看似合理的攻击。

该公开中提出的场景是具有多个客户端的流氓接入点。攻击者可以扫描私有地址空间 10。*.*.*例如，发现网络上的所有 VPN 客户端。除非客户端的防火墙配置为阻止它，否则当探测到正确的 IP 地址时，VPN 接口会很高兴地响应扫描。

一旦找到目标，下一步就是找出一个活动的 TCP 连接。攻击者看不到 VPN 内部的数据，但可以看到数据包的大小和频率。发送带有欺骗源地址的 TCP SYN 数据包将会根据它是否与地址和端口匹配而触发不同的响应。请记住这里的地址和端口空间:攻击者可以对远程端口进行有根据的猜测，并且已经获得了目标的 IP 地址。远程 IP 地址和目标的源端口仍然需要猜测。

发现地址和端口后，TCP 序列号和 ACK 号都可以通过类似的方式发现，包括 VPN 数据包的大小和时间。一旦攻击者掌握了所有这些信息，他就可以将数据注入 TCP 流，但不能从 VPN 内部读取数据。HTTPS 连接仍然可以完全抵御这种攻击，因此它在现实世界中的价值有限。尽管如此，这是一次聪明的攻击，由此带来的修复将使整个网络更加安全。

当我听说这次攻击时，我联系了 Wireguard 的创建者[Jason Donefeld],并询问了这个漏洞的状态。

> WireGuard 的 wg-quick(8)在 oss-sec 上发布
> 公告之前就已经有了缓解措施。

[Jason]忙了几天，Wireguard 终于[进入了 Linux net-next](https://www.phoronix.com/scan.php?page=news_item&px=WireGuard-Net-Next-Lands) 树，这意味着它应该在 5.6 版本中登陆。我很高兴听到已经对这个问题进行了修复，并期待着 Wireguard 正式包含在 Linux 中。

### 星期二补丁

周二的 Windows 补丁[包含了相当多的漏洞](https://www.zdnet.com/article/microsoft-december-2019-patch-tuesday-plugs-windows-zero-day/)，包括一个在野外被积极利用的特权升级。那个零日，CVE-2019-1458，正在和[一个 Chrome 零日](https://securelist.com/windows-0-day-exploit-cve-2019-1458-used-in-operation-wizardopium/95432/)一起使用。Chrome 漏洞是一个竞争条件，导致免费后使用。这两起事件被认为是 WizardOpium 攻击的一部分，该攻击主要通过韩国网站传播。

第二个漏洞 CVE-2019-1468 于本周二被修补。它并没有被积极利用，但却是字体处理代码中的一个 bug。文档或网站可能会嵌入恶意字体，只要显示出来就可以执行任意代码。这个漏洞是一个很好的例子，说明为什么在 2020 年 1 月之后运行 Windows 7 是一个危险的命题。这个会修好，但下一个不会。

### 掠夺金库

研究人员从超频的世界里偷了一出戏，发现[低估某些英特尔处理器](https://arstechnica.com/information-technology/2019/12/scientists-pluck-crypto-keys-from-intels-sgx-by-tweaking-cpu-voltage/)会导致安全 CPU 飞地出错。研究人员称这种攻击为[掠夺电压](https://www.plundervolt.com/)，他们使用一个未记录的指令来动态改变 CPU 电压，并改变受保护的位。

英特尔迅速做出反应，并发布了一个微码更新来解决该问题。这一缺陷一直影响到英特尔第九代处理器。[全文](https://www.plundervolt.com/doc/plundervolt.pdf)有，去看看了解更多。

### 戒指

最近的新闻很热门，尤其是令人毛骨悚然的“网络黑客”在家中通过环形摄像机与孩子们交谈的视频。看晚间新闻，听播音员报道这种近乎神秘的黑客活动是很幽默的。让我们看看能否揭开神秘的面纱。

显而易见的起点是密码重用。很可能我们都至少有一个账户[暴露在数据泄露](https://haveibeenpwned.com/)中。不幸的是，其中许多漏洞包括明文密码。一个让你的账户暴露的非常快速的方法是重复使用已经暴露的用户名和密码。Ring 声称，每次账户泄露都是弱密码或密码重复使用以及缺乏双重身份认证的结果。

似乎有一个工具已经在论坛中传播，该工具加载用户名/密码列表，并试图通过代理列表登录到 Ring service。这些代理允许攻击者并行地进行许多猜测，而不会使 Ring 的强力缓解措施失败。这些账户几乎肯定不是针对被破解的账户，他们只是不幸的人。

Vice 的主板发现了一些关于这些恶作剧背后的额外信息。显然，一个名为 NulledCast 的播客专门在广播中钓人。这些事件似乎是播客的一部分，恶作剧的人并不打算吸引这么多的注意力。