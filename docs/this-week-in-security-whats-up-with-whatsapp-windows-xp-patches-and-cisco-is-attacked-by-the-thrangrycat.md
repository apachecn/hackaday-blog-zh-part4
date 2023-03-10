# 本周安全:Whatsapp、Windows XP 补丁和思科被 Thrangrycat 攻击是怎么回事

> 原文：<https://hackaday.com/2019/05/21/this-week-in-security-whats-up-with-whatsapp-windows-xp-patches-and-cisco-is-attacked-by-the-thrangrycat/>

Whatsapp 允许端到端的加密消息，安全的 VoIP 通话，以及直到本周，当接到电话时安装[恶意软件](https://www.facebook.com/security/advisories/cve-2019-3568)。恶意构建的 SRTCP 连接可触发缓冲区溢出，并在目标设备上执行代码。这个漏洞显然是由一家名为 NSO 集团的监控公司首先发现的。NSO 以 Pegasus 而闻名，这是一个商业间谍软件程序，他们向政府和情报机构推销，该程序涉嫌多起侵犯人权事件和[甚至贾马尔·哈肖吉](https://www.nytimes.com/2018/12/02/world/middleeast/saudi-khashoggi-spyware-israel.html?action=click&module=Top%20Stories&pgtype=Homepage)遇刺事件。看起来这个 Whatsapp 漏洞是[飞马项目](https://www.nytimes.com/2019/05/13/technology/nso-group-whatsapp-spying.html)使用的感染媒介之一。在独立发现漏洞后，脸书周一推送了一个固定客户端。

### windows xp 修补了可使用的漏洞

今年是哪一年！？本周二，微软发布了 Windows XP 的补丁，五年前对这一古老操作系统的支持正式结束。让人想起上次微软给 Windows XP 打补丁，当时 [Wannacry](https://hackaday.com/2017/05/12/massive-cyber-attack-cripples-multiple-uk-hospitals/) 就是危机。本周，微软修补了一个远程桌面协议(RDP)漏洞， [CVE-2019-0708](https://blogs.technet.microsoft.com/msrc/2019/05/14/prevent-a-worm-by-updating-remote-desktop-services-cve-2019-0708) 。该漏洞允许攻击者连接到 RDP 服务，发送恶意请求，并控制系统。由于不需要身份验证，该漏洞被认为是“可被蠕虫利用的”，或者可被自我复制程序利用。

从 Windows XP 到 Windows 7 都有这个缺陷，修复程序已经推出，但显然不是针对 Windows Vista 的。据报道，可以下载 Server 2008 的补丁并手动应用到 Windows Vista。也就是说，是时候淘汰不受支持的系统了，或者至少将它们从网络上断开。

### 有史以来最糟糕的漏洞名称

Thrangrycat 。或者更准确地说，”😾😾😾”是 Cisco 产品中新公布的漏洞，由 Red Balloon Security 发现。思科在许多设备上使用安全引导，以防止恶意篡改设备固件。安全引导是通过使用辅助处理器，即信任锚模块(TAm)来实现的。该模块确保系统的其余部分运行正确签名的固件。这种方案的唯一问题是专用 TAm 也有固件，并且该固件可能被攻击。TAm 处理器实际上是一个 FPGA，研究人员发现可以修改 FPGA 比特流，完全击败安全引导机制。

此次攻击的名称 thrangrycat 可能是对其他荒谬漏洞名称的讽刺。撇开命名问题不谈，这是一项令人印象深刻的工作，编号为 [CVE-2019-1649](https://tools.cisco.com/security/center/content/CiscoSecurityAdvisory/cisco-sa-20190513-secureboot) 。与此同时，Red Balloon Security 披露了另一个漏洞，该漏洞允许经过身份验证的用户进行命令注入。

### 零碎东西

*   谷歌发现[他们的蓝牙安全密钥使用蓝牙](https://security.googleblog.com/2019/05/titan-keys-update.html)，也许这不是一个好主意。
*   我们自己的 Bob Baddeley 最终[结束了超微服务器的故事](https://hackaday.com/2019/05/14/what-happened-with-supermicro/)，可能。
*   五十年前的航空技术是可以被破解的，但可能不会被破解。

看到一个你认为我们应该报道的安全新闻吗？在小费罐里给我们留个条吧！