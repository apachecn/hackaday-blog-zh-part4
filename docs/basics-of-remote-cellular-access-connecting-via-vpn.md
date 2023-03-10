# 远程蜂窝接入基础:通过 VPN 连接

> 原文：<https://hackaday.com/2021/01/14/basics-of-remote-cellular-access-connecting-via-vpn/>

你有一台通过崭新的蜂窝调制解调器连接到互联网[的机器，你计划远程管理它。您快速检查外部 IP，并尝试从另一台 PC 登录。尽管你可以尝试，SSH 就是不能连接。怎么回事？](https://hackaday.com/2020/12/18/basics-of-remote-cellular-access-choosing-a-modem/#comment-6306361)

现代互联网的现实是，大多数客户端不再拥有自己唯一的 IPv4 地址。已经没有足够的食物了。相反，大多数电信运营商使用[电信级网络地址转换](https://en.wikipedia.org/wiki/Carrier-grade_NAT)，允许许多客户共享一个外部地址。这可能会妨碍外部世界的直接连接尝试。即使事实并非如此，大多数手机运营商在默认情况下还是会屏蔽入站连接。然而，有一种方法可以解决这个难题——使用 VPN。

## 一个私有的虚拟网络

![](img/e0da6cb3f4dc55c213631ee43f37f07b.png)

A VPN allows two or more systems connected to the Internet to behave as if they’re on a local network. This is useful for remote administration, particularly when working with cellular connections with restrictive traffic rules.

VPN，或虚拟专用网络，正如它们听起来的那样。它们是一种私有网络，存在于更大的公共网络(如互联网)上的客户端之间。当涉及到通过蜂窝连接与远程主机建立连接时，它们是完成工作的完美工具。让远程主机连接到 VPN 服务器可以避免拒绝传入连接的问题，因为所有流量都通过远程主机自己发起的 VPN 隧道。此外，这意味着连接到 VPN 的其他主机可以像本地网络上的另一台机器一样与远程主机对话。通过正确的设置，VPN 可以是一种高度安全和灵活的与远程机器进行对话的方式，而只需最少的大惊小怪和虚张声势。

可以在家里运行自己的 VPN 服务器，没有太大的麻烦。你需要一台能可靠上网的电脑，它能接受外来的连接。通常，这将涉及在您的家庭路由器上启用端口转发，以便在特定端口上连接到您的家庭 IP 地址的连接被转发到运行 VPN 服务器软件的计算机。此外，您需要确保您的家庭互联网连接不在电信级 NAT 之后。一般来说，如果你有电缆、ADSL 或光纤，只需给你的 ISP 打个电话就可以了。但是，在某些情况下，您可能会发现您必须升级到更高层的连接包才能获得这种待遇。也不需要有一个静态 IP；动态 DNS 服务可以让您的远程系统轻松地呼叫总部。如果你愿意，你甚至可以运行自己的动态域名系统。

所以，假设你有一台备用电脑，一台路由器，它有一个通向更广阔的互联网的开放端口，你所需要做的就是安装正确的软件。OpenVPN 是运行 VPN 服务器的一个流行的选择，它拥有所有需要的功能，并且是免费的。过去，[需要大量的设置](https://openvpn.net/community-resources/how-to/)来安装和生成所有需要的加密证书，然而，[随着 OpenVPN 访问服务器](https://openvpn.net/quick-start-guide/)的发布，入门变得更加简单。

然而，还有其他选择。PageKite 是一个开源的 VPN 解决方案，旨在使连接远程系统变得轻而易举。[在讨论如何从任何地方连接到 Raspberry Pis 时，我们已经在](https://pagekite.net/)之前介绍过它。它可以在付费的基础上获得，一些数据通过 PageKite 的云服务器，使一切更容易设置。推荐价格仅为每月 3 美元，对于更认真的用户，价格可升至每月 6 美元。如果你只需要让你的远程系统在线对话[而没有很多不必要的麻烦，这是一个很好的开始方式。](https://hackaday.com/2016/08/09/yak-shaving-hacker-mode-vs-maker-mode/)另一个解决方案是 [WireGuard](https://www.wireguard.com/#conceptual-overview) ，这是一个基于易用、快速和简单概念的开源 VPN。有了适用于各种流行操作系统的客户机，就可以轻松地启动和运行，而不必大惊小怪。

一旦你让你的远程主机连接到 VPN，管理就很容易了。只需启用 SSH 或您喜欢的远程管理协议，然后登录，就像机器在您的本地网络上一样。如果您的远程机器配置正确，可以保持连接并在掉线时重新连接，那么无论它在世界的哪个地方，只要它有良好的蜂窝数据连接，您都应该可以控制它。只要确保在你将它部署到一个遥远的地方之前，你已经让它在启动时连接到 VPN 否则你第一次需要命令重启时就要倒霉了。

如果您一直在关注本系列，现在您应该有信心选择合适的硬件和软件来通过蜂窝网络远程控制计算机。当然，随着蜂窝网络的漫游自由，随之而来的困难是，您的远程系统可能会位于很远的地方，难以访问。如果出现问题，这可能会使解决问题变得昂贵和复杂。在以后的文章中，我们将探索最小化这些问题的方法，以及如何最好地阻止事情向侧面发展。在那之前，祝你黑客生涯愉快！