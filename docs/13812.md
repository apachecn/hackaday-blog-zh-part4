# 本周在安全:Follina，开放重定向 RCE，和安诺威尔

> 原文：<https://hackaday.com/2022/06/03/this-week-in-security-follina-open-redirect-rce-and-annoyware/>

取决于你问谁，要么 Follina 有两个漏洞，只有一个，要么根据微软一周前的说法，没有任何安全问题。上个月 27 号，有一个`.docx`文件上传到 VirusTotal，那里的大部分工具都认为完全正常。对于[@nao_sec]来说，这似乎不太对，他在 Twitter 上发出了警告。这个可疑文件似乎来自白俄罗斯的某个地方，它使用一系列技巧来运行恶意的 PowerShell 脚本。

> 有趣的 maldoc 是白俄罗斯提交的。它使用 Word 的外部链接来加载 HTML，然后使用“ms-msdt”方案来执行 PowerShell 代码。[https://t.co/hTdAfHOUx3](https://t.co/hTdAfHOUx3)pic.twitter.com/rVSb02ZTwtT2
> 
> —nao _ sec(@ nao _ sec)[2022 年 5 月 27 日](https://twitter.com/nao_sec/status/1530196847679401984?ref_src=twsrc%5Etfw)