# 本周安全:网络安全管理软件产品和火眼，分布式拒绝服务，和增强！

> 原文：<https://hackaday.com/2020/12/18/this-week-in-security-solarwinds-and-fireeye-wordpress-ddos-and-enhance/>

本周的大新闻是太阳风。这家 IT 管理公司供应网络监控和其他安全设备，似乎早在去年春天的一次产品更新[中就包含了恶意代码。他们的设备出现在众多备受瞩目的网络中，如 Fireeye、美国政府的许多分支机构，以及你能想到的几乎任何其他大公司。说这次供应链攻击是一件大事是轻描淡写。责任最初被归咎于 APT42，又名俄罗斯黑客专家。](https://www.fireeye.com/blog/products-and-services/2020/12/global-intrusion-campaign-leverages-software-supply-chain-compromise.html)

这次攻击并不是没有一些积极的影响，因为 Fireeye 已经[发布了一些开源的内部工具。微软领导了官方对攻击的回应，设法在法庭上赢得了 T2 对 T4 C 域名的控制权，并将其黑入 T3。](https://www.fireeye.com/blog/threat-research/2020/12/unauthorized-access-of-fireeye-red-team-tools.html)

这个故事的最后一点是两家投资公司出售太阳风股票的有趣时机。如果这些公司意识到了这一漏洞，并在消息公开之前出售了他们的股票，这将是一个典型的非法内幕交易案例。

## 拒绝服务

攻击者滥用功能的巧妙方法总是让我感到惊讶。在这种情况下，[WordPress ping back 函数可以被用来帮助 DDoS 攻击](https://www.secjuice.com/make-wordpress-pingback-great-again/)。

回顾一下历史，什么是 WordPress pingback？很简单。假设你有一个 wordpress 博客，你可以在上面写一篇新文章。其他人喜欢你的文章以至于链接到他们自己的 WordPress 网站上。如果两个站点都启用了 pingbacks，wordpress 实例将会自动相互对话，并在原始文章上生成 pingbacks 评论。它很聪明，但用途有限，所以许多网站都禁用了这一功能。

问题是，攻击者可以直接连接到许多 WordPress 站点的 pingback API，并宣布一个来自目标站点的新 pingback。然后，这些站点中的每一个都将尝试打开一个新的连接来验证 pingback 公告，从而有效地放大 DDoS 攻击。

你可能认为你的内容分发服务会照顾你。Cloudflare 之类的可以认为是分布式缓存。您请求一个受保护的站点，DNS 名称解析为 Cloudflare 的一个 IP 地址。Cloudflare 使用一些神奇的路由技巧( [anycast](https://blog.cloudflare.com/cloudflares-architecture-eliminating-single-p/) )来自动将您的连接路由到最近的数据中心。然后，Cloudflare 可以代理您的连接，或者在流量高峰期间提供缓存的内容。这种保护的一个重要因素是，公众不会直接连接到您的服务器的 IP 地址，这可以保护您免受 DDoS 攻击。

除非一个 WordPress 站点建立得特别仔细，否则 pingback 响应会泄露真实的 IP 地址，从而可以绕过它。哎哟。

## 最严重的安全问题

思科在 2018 年受到了书中最古老的安全漏洞的攻击。这一无法修补的漏洞导致 456 台虚拟机和 16，000 多个 Webex 帐户被删除。清理工作的费用超过 200 万美元。这是什么漏洞？拥有管理特权且心怀怨恨的员工。离开思科五个月后，[Sudish Ramesh]仍然持有有效证件，这并不能很好地反映思科在人力资源方面的安全做法。Ramesh 将服刑两年，并支付小额罚款。

## 增强！—呃，去哌醋甲酯？

这是一个经典的电影比喻，从《银翼杀手》到《麦吉弗》无处不在——“放大那个部分，增强图像。”(警告，tvtropes。)我们喜欢拿这个开玩笑，但事实证明，在少数情况下这是可能的。[Sipke Mellema]把工作放进去，并给我们带来了[去钉工具](https://github.com/beurtschipper/Depix)。Depix 旨在对像素化图像背后的原始文本进行最佳猜测，假设您知道它所用的字体和其他一些细节，它可能是一个从编辑不当的图像中提取密码和其他数据的有用工具。更多细节，[查看他的文章](https://www.linkedin.com/pulse/recovering-passwords-from-pixelized-screenshots-sipke-mellema)。

 [https://www.youtube.com/embed/LhF_56SxrGk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/LhF_56SxrGk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[Sevron Kitsune]在提示栏中发送了这条消息！

### OAuth 可能会出错

OAuth 似乎是最近几年开发的较好的安全协议之一。你有一个谷歌或脸书帐户，你可以使用单点登录在任何地方进行认证。OAuth 甚至可以用来运行您自己的身份服务。尽管协议很好，但也有出错的地方。Portswigger 的优秀人员为我们带来了对 OAuth 2.0 的良好概述，以及常见的陷阱。