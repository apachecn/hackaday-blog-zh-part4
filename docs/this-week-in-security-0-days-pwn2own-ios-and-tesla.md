# 本周在安全方面:0-Days、Pwn2Own、IOS 和特斯拉

> 原文：<https://hackaday.com/2020/03/27/this-week-in-security-0-days-pwn2own-ios-and-tesla/>

李林的 DVR 和摄像机正被一个惊人复杂的僵尸网络活动积极利用。在正在进行的活动中，有三个单独的 0 天漏洞被利用。如果你有一个李林制造的设备，去检查固件更新，如果你的设备暴露在互联网上，接受它被破坏的可能性。

这些漏洞包括硬编码的用户名/密码、FTP 和 NTP 服务器字段中的命令注入以及任意文件读取漏洞。仅仅是第一个漏洞就足以说服我避开黑盒 DVR，并让我的 IP 摄像头与更广阔的互联网隔离开来。

### Windows 受到攻击

在多个 Windows 版本之间共享的字体渲染库中的代码[被发现容易受到恶意 Adobe Postscript 字体的攻击](https://portal.msrc.microsoft.com/en-us/security-guidance/advisory/adv200006)。可以构建一个文档，利用这个漏洞在打开时运行任意代码，甚至显示在预览窗格上，[听起来有点耳熟](https://hackaday.com/2019/11/30/this-week-in-securitymalicious-previews-vnc-vulnerabilities-powerwall-and-the-5th-amendment/)。

微软承认这个漏洞，以及它正在被“试图利用这个漏洞的有限的、有针对性的攻击”所利用的事实。[正如已经指出的](https://arstechnica.com/information-technology/2020/03/attackers-exploit-windows-zeroday-that-can-execute-malicious-code/)，那种语言通常意味着在政府赞助的活动中使用了漏洞。微软计划等到 4 月份的补丁周二修复这个错误，主要是因为现在不支持的 Windows 7 中这个问题更严重。

还有一点需要注意的是，此次的 Windows 7 补丁将仅限于扩展支持客户。列出了一些缓解措施，包括注销易受攻击的 DLL。另一个建议的做法是禁用预览窗格，这可能也是对即将出现的漏洞的一个很好的预防措施。

### Pwn2Own 2020

另一个被冠状病毒逼到网上的活动，Pwn2Own 2020 于上周结束。虽然看到会议被取消令人沮丧，但在线活动最终更容易被我们其他人获得。

 [https://www.youtube.com/embed/u1udr7j9MQA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/u1udr7j9MQA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



展示了多个令人印象深刻的攻击，如 Adobe Reader 和 Windows 中的两阶段危害，其中打开 PDF 会直接导致系统级危害。另一个令人印象深刻的演示是虚拟机逃逸，攻击者可以从内部破坏 Virtualbox 虚拟机，并获得对裸机操作系统的访问权限。获得“Pwn 大师”称号的是 Richard Zhu 和 Amat Cama of Fluoroacetate。

### iPhone 上的 Android

还记得 2010 年 iPhone 上的 Linux 吗？他们以[项目沙堡](https://projectsandcastle.org/)的形式回来了。在 iPhone 7 上运行 Android 是一个相当不错的技巧，开发人员认为高质量的硬件模拟是这一令人敬畏的黑客技术的主要推动者。

与沙堡项目携手的是 [Checkrain](https://checkrain.com/) 现在已经对 iOS 13.4 提供实验性支持的消息。

> checkra1n 0.9.9 实验预发布-实验 13.4 支持，也请在其他固件上测试。要在 13.4 上运行，在选项视图中勾选“允许未测试的 iOS 版本”复选框—[https://t.co/dmdZNMHbJh](https://t.co/dmdZNMHbJh)
> 
> —qwertyoruiop(@ qwertyoruiopz)[2020 年 3 月 18 日](https://twitter.com/qwertyoruiopz/status/1240310688746221571?ref_src=twsrc%5Etfw)