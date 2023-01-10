# 本周安全:在 Mudge 我们相信，不要相信应用浏览器，在 Pwn2Own 的 Firefox

> 原文：<https://hackaday.com/2022/08/26/this-week-in-security-in-mudge-we-trust-dont-trust-that-app-browser-and-firefox-at-pwn2own/>

推特上又掀起了一场骚动，但这一次是一名安全研究员在制造噪音，而不是一个古怪的亿万富翁。从 2020 年 11 月到 2022 年 1 月，彼得·扎特科担任 Twitter 的安全主管仅一年多。你可能更了解 Zatko，他叫[Mudge]，是一位著名的安全研究员，[写了一本关于缓冲区溢出的书。他是](https://insecure.org/stf/mudge_buffer_overflow_tutorial.html) [L0pht Heavy Industries](https://en.wikipedia.org/wiki/L0pht) 的成员，在 DARPA 和谷歌工作，并在 Twitter 上被召来回应 2020 年 7 月的黑客攻击，当时许多品牌账户运行比特币扫描。

Mudge 于 2022 年 1 月在 Twitter 上被解雇，似乎他立即开始整理举报投诉。你可以在 archive.org 上访问[他的投诉包，以](https://archive.org/download/whistleblower_disclosure)[告密者 _disclosure.pdf](https://ia601507.us.archive.org/0/items/whistleblower_disclosure/whistleblower_disclosure.pdf) (PDF，和[镜报](https://www.washingtonpost.com/technology/interactive/2022/twitter-whistleblower-sec-spam/whistleblower_disclosure.pdf))为主要文件。这里有一些有趣的花絮，比如 Twitter 上有多少垃圾邮件机器人的真实答案:“我们真的不知道。”非常公开的声明“… [<本季度报告的 mDAU 中有 5%是垃圾邮件帐户](https://twitter.com/paraga/status/1526237585441296385)”有点牵强，因为可货币化的每日活跃用户数本质上被定义为非机器人的活跃帐户。或许马斯克的抱怨比之前想象的更合理。


超过 30%的 Twitter 员工电脑在某种程度上禁用了安全更新，大约一半的 Twitter 员工可以访问生产系统。有一次，[Mudge]觉得有必要“封闭生产环境”，担心内部工程师因政治动荡而故意破坏。令他惊讶的是，没有任何措施来预防甚至追踪这种攻击。另一个令人担忧的发现是缺乏针对多节点故障的灾难计划。细节被编辑了，但一些数据中心同时正常关闭将使 Twitter 的基础设施瘫痪数周或更长时间，需要注意的是，恢复服务将是一个未知难度的挑战。有趣的是，这个场景几乎让 Twitter 在 2021 年春天永久宕机。我在这里要注意的是，这也意味着如果 Twitter 数据中心之间的网络连接中断，Twitter 可能会遭受裂脑的情况。这是高可用性系统中的一种效应，在这种系统中，多个系统以主模式运行，并且共享数据集收敛。

有一些奇怪的反对意见，比如要求[Mudge]口头给出他对问题的初步概述，不要把书面报告发给董事会成员。当你被要求*而不是*写下某事时，这绝不是一个好兆头。后来，[Mudge]请了一家外部公司来准备关于 Twitter 在打击垃圾邮件和机器人问题上做得如何的报告。Twitter 的高管们聘请了一家律师事务所，首先将报告发送给该事务所，在那里他们将最令人尴尬的细节删除，然后才交给[Mudge]。令人震惊。

一个面向 Twitter 工程师的内部系统每天有近 3000 次失败登录。没有人知道为什么，也从来没有解决过。员工工作站没有正常运行的备份，高管们的回应是，这至少给了他们一个不遵守官方记录要求的合理借口。截至今年早些时候，Twitter 估计有 10，000 个服务可能存在 Log4j 漏洞，并且没有可行的计划来解决可能的漏洞。如果你想从 Twitter 获得 bug 奖励，这似乎是一个很好的开始。

事情并没有好转。12 月 16 日，他向 Twitter 董事会提交了一份他认为是欺诈性的报告，他试图在内部揭发此事。这一努力在 Twitter 的内部结构中渗透了一个月，1 月 18 日，他声明他已经准备好向董事会提交一份准确的报告。显然，为了阻止这份报告的发表，[Mudge]在第二天，也就是 1 月 19 日被解雇了。

我最初的反应被马丁·麦凯总结得很好，讽刺的是在推特上。

> 如果要在相信 Mudge 和几乎所有美国 CEO 之间做出选择，我会选择 Mudge。
> 
> —马丁·麦基(@麦基)[2022 年 8 月 23 日](https://twitter.com/mckeay/status/1562049421042487299?ref_src=twsrc%5Etfw)