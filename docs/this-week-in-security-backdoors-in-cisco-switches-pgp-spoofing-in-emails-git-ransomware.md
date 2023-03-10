# 本周安全:思科交换机的后门，电子邮件中的 PGP 欺骗，Git 勒索软件

> 原文：<https://hackaday.com/2019/05/13/this-week-in-security-backdoors-in-cisco-switches-pgp-spoofing-in-emails-git-ransomware/>

思科 9000 系列中的一些交换机容易受到一个远程漏洞的攻击，该漏洞编号为 CVE-2019-1804。实际上，称之为漏洞有点奇怪，因为软件正在按预期运行。Cisco 在发运这些交换机时，在软件中为所有根 SSH 登录硬编码了相同的私钥。拥有密钥的任何人都可以以 root 用户身份登录这些交换机。

思科在他们的公告中提出了一个奇怪的说法，即这只能通过 IPv6 来利用。这看起来很奇怪，因为没有任何关于 SSH 或特定于 IPv6 的密钥认证过程的内容。这表明可能还有另一个错误，他们不小心让 SSH 端口在 IPv6 上对世界开放。另一种可能性是，他们假设所有这些交换机都安全地位于 NAT 路由器之后，因此无法通过 IPv4 访问。IPv6 的优点/缺点之一是没有 NAT，所有网络设备都可以从外部网络访问。(在存在路由的意义上是可访问的。当然，防火墙仍然是可能的。)

令人震惊的是，有多少设备，甚至是高端商用设备，都带有无意但有效的后门，就像这个一样。

### Git 存储库勒索软件

首先，[勒索软件已经瞄准了 Git 库](https://www.zdnet.com/article/a-hacker-is-wiping-git-repositories-and-asking-for-a-ransom/)。GitHub、Gitlab 和其他服务的数百个存储库已被替换为勒索信，要求 0.1 比特币才能恢复。有趣的是，勒索信威胁要公开密码。这是开源肯定要解决的问题。

怎么会有人一下子闯入这么多账户？安全研究公司 Badpackets.net 透露了真相。

> 该死，我以为所有那些。git/config "扫描是无害的。我猜我们现在知道目标是什么了。
> 
> —坏数据包报告(@ Bad _ Packets)[2019 年 5 月 3 日](https://twitter.com/bad_packets/status/1124429828680085504?ref_src=twsrc%5Etfw)