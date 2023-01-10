# 本周安全:Zimbra、Lockbit 2 和 Hacking NK

> 原文：<https://hackaday.com/2022/02/11/this-week-in-security-zimbra-lockbit-2-and-hacking-nk/>

未知攻击者一直在利用针对 Zimbra 电子邮件套件的 0 天攻击。Volexity 的研究人员在去年 12 月首次发现了对 T2 的攻击，这是由他们的监控基础设施检测到的。这是一个跨站点脚本(XSS)漏洞，当打开恶意链接时，恶意页面上运行的 JavaScript 可以访问登录的 Zimbra 实例。攻击活动利用这一漏洞获取电子邮件和附件，并将其上传给攻击者。研究人员还不能确定是哪个组织策划了这些攻击，但一些间接证据指向了一个中国组织。那个证据？时区。攻击者要求所有人使用`Asia/Hong_Kong`时区，所有发送的网络钓鱼邮件的时间与该时区的工作日完全吻合。

[Zimbra 已经回应](https://blog.zimbra.com/2022/02/hotfix-available-5-feb-for-zero-day-exploit-vulnerability-in-zimbra-8-8-15/)，确认了该漏洞并发布了补丁。这场运动似乎是专门针对欧洲政府和各种媒体的。如果您正在运行 Zimbra 实例，请确保您至少运行了`8.8.15.1643980846.p30-1`。

## 锁定位 2.0

因为安全专业人员需要其他东西来让我们有事可做，所以 LockBit 勒索软件活动又回来了，进入第二轮。这是另一个以“即服务”模式运行的勒索病毒活动——RAAS。LockBit 2 已经引起了足够的关注，以至于 FBI 发布了一条关于它的简讯。这是联邦调查局联络警报系统，在竞选最糟糕的缩写。(帮助他们弄清楚下面评论中的“H”代表什么！)

像许多其他勒索软件活动一样，LockBit 有一个触发保释的语言代码列表——你可能会想到的东欧语言。勒索软件运营商长期以来一直试图通过打击自己后院的目标来避免毒化自己的水井。据报道，这款产品也有 Linux 模块，但似乎仅限于 VMWare ESXi 虚拟机。一系列的 IOC 已经公布，联邦调查局要求任何日志，赎金笔记，或其他可能与这次活动有关的证据，如果可能的话发送给他们。

## 不是你要找的含羞草

说到政府通知， [CISA 发布了一份关于含羞草无线产品的建议，基于多份简历，其中三份得到了可怕的 10.0 分。存在不适当的授权问题，例如 API 端点可以在没有授权的情况下被访问；一个服务器端请求伪造问题，这可能允许攻击者通过 web 前端走私消息；一个 SQL 注入；甚至还有用于存储密码的未加盐 MD5 散列法。](https://www.cisa.gov/uscert/ics/advisories/icsa-22-034-02)

这些漏洞是由 Claroty 的研究员 Noam Moshe 发现的。[他公开证实了事情正如看上去那样糟糕，攻击云接口可能会导致现场硬件受损。没有关于这个故事的完整报道，但是到目前为止，它似乎是一个非官方的黑盒安全审计，所以它不是一个官方的代码审查。这些只是有限审计发现的漏洞。请留意更多的问题。](https://www.securityweek.com/critical-flaws-expose-mimosa-wireless-broadband-devices-remote-attacks)

## SAP 支付他们的 Log4j 费用

Log4j 漏洞如此令人头痛的一个原因是，Java 库嵌入在如此多的二进制文件和设备中，需要更新整个二进制文件来修复问题。如果漏洞在`glibc`中，只有那个库可以被更新，但是包含 Log4j 的每个二进制文件都必须单独更新。强调这是一个漫长的过程， [SAP 已经发布了二月份补丁日](https://wiki.scn.sap.com/wiki/display/PSR/SAP+Security+Patch+Day+-+February+2022)的补丁。修复的八大漏洞中有六个是 Log4j。这个会存在很长一段时间。

## 思科 RV 路由器

Cisco RV160、RV260、RV340 和 RV345 小型企业路由器都有[个 RCE 和权限提升漏洞](https://tools.cisco.com/security/center/content/CiscoSecurityAdvisory/cisco-sa-smb-mult-vuln-KA9PK6D)，并提供 PoC 代码。RCE 是一个简单的 HTTP 请求，它绕过了访问控制。其中几个单元还存在命令注入漏洞，用户输入没有得到充分的净化，导致命令在底层系统上执行。虽然补丁是可用的，但思科表示这些缺陷没有解决办法。想想吧。你无法锁定这些设备来阻止 RCE 病毒。再一次，去你的网络储藏室，看看是否有一个隐藏在那里的某个地方。

> 该死，我们试图给蓝队一些时间来修补，但它在这里。我们的漏洞就在我们与 [@pedrib1337](https://twitter.com/pedrib1337?ref_src=twsrc%5Etfw) 在[@ offensive _ con](https://twitter.com/offensive_con?ref_src=twsrc%5Etfw)
> CVSS 10 思科 AnyConnect VPN 网关
> CVE-2022—20699[https://t.co/EnwAOvvG1j](https://t.co/EnwAOvvG1j)交谈后弹出
> 
> —拉多·RC1(@ rabbit pro)[2022 年 2 月 5 日](https://twitter.com/RabbitPro/status/1489978906597859333?ref_src=twsrc%5Etfw)