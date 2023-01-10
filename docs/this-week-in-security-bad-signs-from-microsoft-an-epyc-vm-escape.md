# 本周安全:来自微软的坏信号，Epyc 虚拟机逃逸

> 原文：<https://hackaday.com/2021/07/02/this-week-in-security-bad-signs-from-microsoft-an-epyc-vm-escape/>

代码签名是将我们从恶意软件中拯救出来的银弹，对吗？没有那么多，特别是当[供应商被说服签署恶意代码](https://arstechnica.com/gadgets/2021/06/microsoft-digitally-signs-malicious-rootkit-driver/)的时候。G DATA 的研究人员发现了一个 Windows 内核驱动程序，表明它可能是恶意的。这似乎很奇怪，因为驱动程序是由微软正确签名的。经过进一步调查，很明显这确实是恶意软件。该文件被报告给微软，签名被撤销，恶意软件被添加到 Windows Defender 定义中。

微软官方的回应很奇怪。他们首先向每个人保证，他们的驱动程序签名过程实际上没有受到影响，就像你一样。接下来的部分很奇怪。谈论恶意软件背后的人:“演员的目标是使用驱动程序来欺骗他们的地理位置，以欺骗系统，并从任何地方玩。该恶意软件使他们能够在游戏中获得优势，并可能通过键盘记录器等常用工具泄露他们的帐户来利用其他玩家。”这似乎与观察到的恶意软件的行为不符——它似乎正在解码 SSL 连接并将数据发送到 C & C 服务器。如果有新的消息，我们会通知你的。


## 逃离科索沃核查团

让我们来谈谈虚拟化，特别是 AMD 硬件的 KVM 代码中的一个缺陷。有几个区别可以让这个更容易理解。首先，Linux 中的虚拟化分为两个不同的部分。内核虚拟机(KVM)是在内核中运行的驱动程序，处理繁重的工作，如内存管理、调度和向 CPU 发送控制指令。另一半是用户空间部分，这里最广泛使用的项目是 QEMU。这个漏洞是值得注意的，因为它存在于 KVM 代码本身中，这意味着它运行在内核空间中。

我们的错误围绕着在嵌套虚拟化环境中如何处理`VMRUN`指令。此指令获取一个数据块，并初始化一个新运行的虚拟机。当它从一个已经运行的 VM 中被调用时，该数据会被检查，然后在被传递到底层 KVM 之前被复制。这个过程是潜在的问题，因为检查然后复制过程不是原子过程。换句话说，在执行检查之后，但在数据实际发送到虚拟化堆栈之前，可以修改嵌套的虚拟机初始化数据，这是一个检查时使用时(TOCTOU)漏洞。

还有一个更重要的概念。裸机上的 KVM 模块处理所有虚拟机的启动，甚至是嵌套的虚拟机。所有的`VMRUN`调用都必须通过虚拟机管理程序内核，以获得硬件虚拟化加速。VMRUN 数据的一个位是 KVM 是否应该截取该指令的指示符。不支持将该位设置为 0，只会取消该过程。问题是当一个嵌套的 VM 调用这个命令时，但是外部 VM 中的一个进程在检查之后设法将该位更改为 0。这会导致代码以非预期的方式运行，用内部虚拟机数据覆盖外部虚拟机的配置。

为了真正利用这个 TOCTOU 错误，外部虚拟机权限被覆盖，从而使虚拟机能够更好地访问底层硬件。其中一个权限允许 VM 为一个`VMEXIT`调用重写保存的上下文地址。因此，通过一些其他技巧，虚拟机可以利用 TOCTOU 漏洞为自己提供这种权限，构建一个恶意上下文，并欺骗裸机 KVM 进程切换到该恶意上下文，从而让攻击者控制系统。我在这里掩盖了一堆细节，所以如果你想要完整的细节，去看看完整的报道，由 Project Zero 的[Felix Wilhelm]专业地整理。

## Linkedin 数据

一个拥有 7 亿 Linkedin 用户的数据库[在一个论坛](https://www.privacysharks.com/exclusive-700-million-linkedin-records-for-sale-on-hacker-forum-june-22nd-2021/)上公开出售，100 万份样本被作为良好数据的证据发布。某些网站称这是违规行为，这并不完全正确，因为这些数据似乎是从 Linkedin API 中抓取的，不包括密码哈希或私人信息。这似乎与四月份报道的[的数据集基本相同，可能更新了新的条目以弥补数字上的差异。](https://9to5mac.com/2021/04/09/500m-accounts-scraped-linkedin/)

## 我的书的故事继续

上周，我们告诉你我的书被远程擦除，我推测这可能是一个勒索软件活动出错。看起来这根本不是勒索软件，而是有人在远程攻击后掩盖了他们的踪迹。这里实际上有两个漏洞。之前已知的 CVE-2018-18472 似乎已被用于在可访问互联网的设备上安装恶意二进制文件。目前还不知道这个二进制文件到底做了什么，但可能是类似僵尸网络的活动。无论如何，第二个 0 天漏洞 CVE-2021-35941 被用来触发远程工厂重置。早期的理论是，二进制文件是由一个攻击者部署的，其他人触发了重置，但 [WD 的分析](https://www.westerndigital.com/support/productsecurity/wdc-21008-recommended-security-measures-wd-mybooklive-wd-mybookliveduo)发现，在某些情况下，两次攻击都是从同一个 IP 发起的。希望随着对双星系统的研究，更多的故事会浮出水面。

## Zyxel 0 天

Zyxel 发布了对最近一连串设备妥协事件的回应。到目前为止，他们的回应在细节上非常简短，最明显的是缺乏 CVE，被利用的漏洞的细节，或实际修复漏洞的固件。

> 威胁参与者试图通过 WAN 访问设备；如果成功，他们将绕过身份验证，与未知用户帐户建立 SSL VPN 隧道。

这篇文章非常着重于如何防止攻击者从互联网访问暴露的 web 接口，但在我看来，最大的问题是攻击者如何能够轻松地“绕过认证”。攻击者可能只是在运行一个密码列表，而 Zyxel 固件中没有足够的速率限制。不过，我怀疑这是一个在野外被利用的 0 天漏洞。

据我所知，自从这个通知首次公布以来，已经过去了一周多，Zyxel 仍然没有透露他们是否有 0-day 在玩。那是不负责任的。话说回来，Zyxel [没有](https://threatpost.com/cybercriminals-exploits-zyxel-flaw/162789/) [确切地说](https://www.zyxel.com/us/en/support/remote-code-execution-vulnerability-of-NAS-products.shtml)拥有[在](https://www.zyxel.com/support/Zyxel-security-advisory-for-command-injection-vulnerability-of-firewalls.shtml)[产品安全](https://pierrekim.github.io/blog/2020-03-09-zyxel-secumanager-0day-vulnerabilities.html)方面的最佳记录。

## RPM 的问题

啊，红帽包装经理。在某种程度上，它定义了 Linux 发行版应该是什么样子，有体面的软件管理和难以破解的更新。说真的，如果我只能改变非自由操作系统的一件事，那就是将整个操作系统转移到 RPM 或 dpkg 之类的东西上。立即更有用，但我跑题了。

CentOS forks 的一个好处是，越来越多的人开始关注基于 RPM 的系统背后的代码。结果，发现了一些问题，比如, [RPM 没有检查证书撤销或过期的情况。这听起来像是一个可怕的漏洞，但是请记住，使用证书撤销根本不是计划的一部分。该特性从未实现，因为它从未被需要或使用过。另一方面，缺乏验证意味着如果一个发行版失去了对其中一个签名密钥的控制，他们将很难控制这个问题。不管是哪种方式，补丁都是在 RPM 的 OpenPGP 实现中添加检查。](https://www.zdnet.com/article/major-linux-rpm-problem-uncovered/)

## 禁用打印假脱机程序以避免打印噩梦

今年 6 月，CVE-2021-1675 修补了一个 Windows 漏洞，允许 RCE 使用后台打印程序。看来微软的补丁是一个糟糕的补丁，阻止了一个特定的漏洞，而不是修复真正的问题。一旦补丁作为补丁星期二的一部分被推出，多个[POC 被披露](https://github.com/afwu/PrintNightmare)，但令人惊讶的是[其中一些仍然工作](https://github.com/cube0x0/CVE-2021-1675)！仍在工作的漏洞利用[被追踪为 CVE-2021-34527](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-34527) 。快速浏览一下 PoCs 似乎表明，这是一种将未签名的打印机驱动程序推入提供远程打印的机器的方式。

这个漏洞很容易被利用，并且可以利用，所以预计攻击者很快就会把它加入他们的锦囊妙计中。这已经足够严重了，微软和 CISA 建议我们所有人[关闭域控制器上的后台打印程序](https://us-cert.cisa.gov/ncas/current-activity/2021/06/30/printnightmare-critical-windows-print-spooler-vulnerability)，以及任何不需要打印的系统。