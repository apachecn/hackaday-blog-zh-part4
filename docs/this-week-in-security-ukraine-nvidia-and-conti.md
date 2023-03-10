# 本周安全:乌克兰、Nvidia 和 Conti

> 原文：<https://hackaday.com/2022/03/04/this-week-in-security-ukraine-nvidia-and-conti/>

围绕入侵乌克兰的地缘政治超出了本专栏的范围，但网络安全的影响无疑是合适的素材。这里的挑战是，上周发生的几乎所有值得注意的事情最初都与冲突有关，但在一些情况下，报道的联系没有经受住审查。我们确实知道乌克兰副总理在推特上呼吁“网络专家”追踪一份俄罗斯企业和国家机构的名单。名单上的许多网站确实关闭了一段时间，这在数字上相当于[撕掉一张海报](https://xkcd.com/932/)。作为回应，俄罗斯最大的 ISP 停止向一些目标站点发布 BGP 路由，有效地终止了任何来自外部的攻击。

过去一周，一些类似的事件已经发生，比如俄罗斯的电动汽车充电站拒绝充电，并展示了一条政治信息，“光荣属于乌克兰”。并非所有的攻击都如此微不足道。Eset 的研究人员已经识别出 HermeticWiper ，这是一种除了破坏数据之外没有其他目的的恶意软件。它已经在数百个高价值目标上被发现，很可能造成很大的破坏。这很可能是同一种恶意软件，微软[称之为 FoxBlade，并公布了他们的回应细节](https://arstechnica.com/gadgets/2022/03/microsoft-identifies-and-mitigates-new-malware-targeting-ukraine-within-3-hours/)。

## 孔蒂泄漏

在非常相关的新闻中，孔蒂勒索软件团伙宣布，他们将报复西方对俄罗斯或俄语地区的网络攻击。他们的声明全文转载于此。

> 作为对西方好战分子和美国威胁对俄罗斯联邦公民使用网络战的回应，孔蒂团队正式宣布，如果西方好战分子试图以俄罗斯或世界上任何讲俄语的地区的关键基础设施为目标，我们将利用我们的全部能力实施报复措施。我们不与任何政府结盟，我们谴责正在进行的战争。然而，众所周知，西方发动战争的主要目标是平民，如果和平公民的福祉和安全因美国的网络侵略而受到威胁，我们将动用我们的资源进行反击。

这自然招致了一些强烈的批评，最有趣的是来自推特账户的批评。顾名思义，这个账号是在发布 Conti 成员之间的内部聊天记录。有两种流行的理论。首先，这些泄密者是孔蒂的一名前成员，一名乌克兰人，他对他们声称支持俄罗斯非常生气。[另一种说法是由【KrebsOnSecurity】](https://krebsonsecurity.com/2022/03/conti-ransomware-group-diaries-part-i-evasion/)报道的，这是一名乌克兰安全研究员，但不是以前与孔蒂有联系的人。这导致了许多问题，比如日志是如何被访问的。无论哪种方式，我们得到了一个相当有趣的研究孔蒂基础设施。

> Conti 勒索软件泄露已经揭示了 Conti 的主要比特币地址。
> 
> 从 2017 年 4 月 21 日至 2022 年 2 月 28 日，康帝已收到 65，498.197 BTC
> 
> 即 2，707，466，220.29 美元。[pic.twitter.com/sUdRnkLsoo](https://t.co/sUdRnkLsoo)
> 
> —VX-underground(@ vxunderground)[2022 年 2 月 28 日](https://twitter.com/vxunderground/status/1498394338027610124?ref_src=twsrc%5Etfw)