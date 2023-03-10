# 本周安全:诈骗联邦调查局，在野外，和人工智能安全

> 原文：<https://hackaday.com/2022/12/16/this-week-in-security-scamming-the-fbi-in-the-wild-and-ai-security/>

如果你是政府字母机构的一部分，特别是运行一个共享信息以打击网络犯罪的程序，确保在接纳新成员前正确验证新成员的身份。哦，还要确保 API 是有速率限制的，这样恶意成员就不能抓取整个用户数据库并在黑暗的网络论坛上出售。

抛开 snark 不谈，这正是 FBI infra guard 项目所发生的事情。一个聪明的用户用一个 CEO 的名字和电话号码，以及一个看起来很有说服力的电子邮件地址申请了这个程序。项目管理员没有做太多的尽职调查，就批准了申请。尴尬。

## BSD Ping

首先，FreeBSD 的好人们发布了一些关于我们上周谈到的 ping 问题的勘误表。首先，请注意，虽然 ping 确实通过 setuid 提升了 root 权限，但是在进行任何数据处理之前，这些权限就会被删除。FreeBSD 上的 ping 在一个[辣椒沙盒](https://www.cl.cam.ac.uk/research/security/capsicum/)中运行，这是 ping 内部对系统危害的一个巨大障碍。最后，在现实环境中对该错误的进一步检查对远程代码执行(RCE)由于堆栈布局实际上是可能的这一想法提出了质疑。

> 如果有人在某个地方搞砸了，去看看你是否在其他地方以同样或相似的方式搞砸了。

OpenBSD 开发人员[Florian Obser]的明智建议。因此看到 FreeBSD 中的 ping 问题，他开始[检查 OpenBSD ping 实现是否有相同或相似的问题](https://tlakh.xyz/fuzzing-ping.html)。易受攻击的代码不会在不同版本之间共享，所以他使用了 afl++，这是一个模糊工具，拥有[令人印象深刻的发现列表](https://aflplus.plus/)。将 afl++连接到 ping 中处理传入数据的函数，看看有什么变化。结论呢？在这次特别的努力中没有发现崩溃，但是发现并修复了几个挂起。这就是胜利。

## 野生的 Citrix

Citrix ADC (应用交付控制器)中的一个[漏洞，一个用于复杂 web 应用的负载平衡器，正在被积极利用。这一事件促使美国国家安全局向](https://www.citrix.com/blogs/2022/12/13/critical-security-update-now-available-for-citrix-adc-citrix-gateway/)[发布了一份 PDF 格式的公告](https://media.defense.gov/2022/Dec/13/2003131586/-1/-1/0/CSA-APT5-CITRIXADC-V1.PDF)，将攻击归咎于 APT5，认为 apt 5 是一名伊朗演员。

真正的漏洞是一个老漏洞，显然是几年前悄悄地修复的。现在才发现这是一个严重的问题，它允许远程危及配置为执行 SAML 身份验证的易受攻击设备。现在已经为多个易受攻击的版本提供了补丁程序，并且已经发布了折衷指标(IoCs)。

## SPNEGO NEGOEX

这一节的标题有强烈的运动鞋共鸣，我的眼睛一直试图重新排列成“太多的秘密”，但它就是不适合。“否定”指的是延伸否定。“SPNEGO”是“简单且受保护的 GSSAPI 协商机制”的缩写。当然，GSSAPI 是“通用安全服务应用程序接口”。所有这些字母汤最终归结为一种协商认证协议的方法。重要的一点是，根据设计，该协议在任何身份验证发生之前运行，并且可以在一系列不同的服务中访问。SMB、RDP、SMTP 甚至 HTTP 都可以公开 SPNEGO 协商。当然，[微软的实现中有一个严重的安全漏洞](https://securityintelligence.com/posts/critical-remote-code-execution-vulnerability-spnego-extended-negotiation-security-mechanism/)。

该漏洞，CVE-2022-37958，已于 9 月修补，并被归类为高严重性。就在几天前，[Valentina Palmiotti]展示了该漏洞可以用于远程执行，并且已经达到了临界严重性。完整的细节将在 2023 年发布，给每个人足够的时间来修补这个。基于目前已经发布的内容，这将是非常重要的。比赛现在开始了，看看是否有任何恶意组织在此之前找出细节。

> 演示 CVE-2022-37958 RCE Vuln。可通过任何进行身份验证的 Windows 应用程序协议访问。是的，这意味着 RDP、中小企业和更多。请贴上这个，很严重！[https://t.co/ikOrTvQIJs](https://t.co/ikOrTvQIJs)pic.twitter.com/bOTmL5Fh2HT2
> 
> ——chompie(@ chompie 1337)[2022 年 12 月 13 日](https://twitter.com/chompie1337/status/1602757336908660736?ref_src=twsrc%5Etfw)