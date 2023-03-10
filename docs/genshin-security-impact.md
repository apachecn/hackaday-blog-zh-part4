# Genshin 安全影响

> 原文：<https://hackaday.com/2022/08/29/genshin-security-impact/>

《Genshin Impact》是一款 MMORPG 游戏，有着可爱的动漫风格的角色，可能从另一个经典的 Nintento 系列中获得了太多的灵感，是一款在 PlayStation、iOS、Android 和 PC 平台上都相对受欢迎的游戏。最后一个已经引起了一些争议，因为 PC 版游戏包括一个运行在 Windows 内核环境中的反作弊内核驱动程序，并且在最初发布的[中，该模块甚至在游戏关闭](https://sea.ign.com/genshin-impact/164292/news/mihoyo-publicly-addresses-genshin-impact-spyware-issue-releases-new-patch-to-fix-it)后仍保持运行。

反作弊驱动程序再次成为新闻焦点，[趋势科技发现了一个勒索软件活动，其中包括反作弊驱动程序`mhyprot2.sys`](https://www.trendmicro.com/en_us/research/22/h/ransomware-actor-abuses-genshin-impact-anti-cheat-driver-to-kill-antivirus.html) ，作为感染的一部分。该模块已知有漏洞，并且仍然是签名的内核驱动程序，因此恶意软件活动加载该驱动程序并使用其功能来禁用反恶意软件保护。

竞选的其余部分很简单。从访问一台连接到域的机器开始，攻击者利用这个立足点来访问域控制器。恶意脚本托管在共享存储上， [PsExec](https://docs.microsoft.com/en-us/sysinternals/downloads/psexec) 用于在所有域成员机器上运行它。这里真正的新颖之处是使用易受攻击的反作弊内核驱动程序作为反恶意软件旁路。据我们所知，这个驱动程序*仍然*被 Windows 签名并认为是可信的。我们呼吁微软撤销这个易受攻击的驱动程序，因为它现在正被恶意软件活动频繁使用。关于安全的更多信息，[请查看我们的每周专栏](https://hackaday.com/tag/this-week-in-security/)，