# 免费 P2P VPN

> 原文：<https://hackaday.com/2020/10/18/free-p2p-vpn/>

人们使用 VPN——虚拟专用网络——有很多原因。然而，对许多人来说，它是隐藏你的网络流量的同义词，这是 VPN 可以做到的一件事。 [FreePN](https://www.freepn.org) 是一个相对较新的开源项目，旨在构建一个免费的点对点 VPN 网络。和 TOR 一样，它是分散的。

现在，你可以为 Ubuntu 和 Gentoo 下载。有一种方法可以让 Debian、Fedora 和 Arch 提前访问。Windows、iOS、MacOS 和 Android 版本是未来的承诺。

代码在 [GitHub](https://github.com/freepn) 上，所以理论上所有问题都是可以回答的。深入研究 fpnd 自述文件告诉了我们希望在主页上找到的大多数功能(但没有找到):

> FreePN 网络守护程序(fpnd)是分布式虚拟专用网(dVPN)的 P2P 实现，它创建了一个匿名的对等“云”,其中每个对等既是客户端节点，也是出口节点。对等体在启动时随机连接，并根据需要重新连接到新的(随机)对等体。
> 
> FreePN 网络守护程序(fpnd)是分布式虚拟专用网(dVPN)的 P2P 实现，它创建了一个匿名的对等“云”,其中每个对等既是客户端节点，也是出口节点。对等体在启动时随机连接，并根据需要重新连接到新的(随机)对等体。

此外，该页面还指出，它们只路由 http(s)流量和可选的 DNS 流量。IPv6 数据包会被丢弃，除非您将其配置为不通过 VPN。

这是比 TOR 更好的答案吗？我们不知道。我们不清楚你如何为一些可能的用例设置这个，但似乎在 Reddit 上有一个羽翼未丰的支持团体。如果这项技术运行良好，能够支持更多的平台，那么对于在线隐私和保护来说，这可能是一件好事。

我们之前已经注意到，真正安全的网络可能[难以实现](https://hackaday.com/2019/12/13/this-week-in-security-vpns-patch-tuesday-and-plundervault/)。对于我们许多人来说，VPN 只是一个额外的安全层，或者是一种只能在另一个国家观看电视的方式。但是对一些人来说，VPN 是一种[政治必需品](https://hackaday.com/2008/08/03/getting-around-the-great-firewall-of-china/)。