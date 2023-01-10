# OmniBallot 是网上投票的又一次有缺陷的尝试

> 原文：<https://hackaday.com/2020/06/14/omniballot-another-flawed-attempt-at-online-voting/>

尽管几十年来，选举中的在线投票一直是一个有争议的话题，但在当前的疫情期间，它受到了更多的关注。与基于邮件的投票一样，它可以成为保持世界民主国家平稳运行的重要工具。这就是由 Democracy Live 制作的 OmniBallot 软件发挥作用的地方，不幸的是，它不适合这个目标。

尽管已经被多个美国司法管辖区用于在线投票，麻省理工学院的[Michael Specter] 和密歇根大学的研究人员进行的一项研究指出了这一基于网络的平台的缺陷。他们的建议是要么完全避免使用 OmniBallot，要么只使用它来打印空白选票，然后用手标记并通过邮件发送。

该软件的一个问题是，默认情况下，它会在 Democracy Live 服务器上创建标记的选票 PDF，而不仅仅是在用户的设备上。另一个原因是，作为一个基于网络的平台，它托管在亚马逊网络服务(AWS)上，JavaScript 源代码来自 CloudFlare 和谷歌服务器。考虑到电子投票机的问题是在投票站的未经授权的访问，它不需要很长的解释就可以看出 OmniBallot 缺乏端到端的安全性提供了许多潜在的攻击面。

当 Ars Technica 联系 Democracy Live 对这些发现进行评论时，Democracy Live 首席执行官[Bryan Finney]回应说“该报告没有发现 OmniBallot 的任何技术漏洞”。由于研究人员没有检查 OmniBallot 代码本身(从技术上来说是正确的)，但忽略了更重要的一点，即缺乏对每个选民的设备以及投票过程中涉及的每个 AWS、CloudFlare 和 Google 实例的安全保证。

因此，OmniBallot 的推荐用途是用于上述空白选票的打印，以节省通常邮寄投票的一半行程时间。