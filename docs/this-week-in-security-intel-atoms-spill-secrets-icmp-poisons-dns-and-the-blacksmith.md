# 本周安全:英特尔原子泄漏秘密，ICMP 毒害 DNS，和铁匠

> 原文：<https://hackaday.com/2021/11/19/this-week-in-security-intel-atoms-spill-secrets-icmp-poisons-dns-and-the-blacksmith/>

英特尔宣布 [CVE-2021-0146，基于凌动架构的某些处理器](https://arstechnica.com/gadgets/2021/11/intel-releases-patch-for-high-severity-bug-that-exposes-a-cpus-master-key/)存在漏洞，可信平台模块(TPM)是问题的核心。围绕 TPM 的系统的目标是即使在攻击者进行物理访问的情况下也能保持系统的完整性，因此使用存储在主板上的安全芯片中的密钥对硬盘进行加密。TPM 芯片持有该加密密钥，并在启动过程中提供该密钥。当与安全引导结合使用时，即使在物理访问的情况下，这也是一种防止篡改或数据访问的非常有效的方法。这是有效的，至少，当一切顺利的时候。

今年早些时候，[我们报道了一个故事，通过点击连接 TPM 和 CPU 的轨迹，可以直接从主板上嗅探到加密密钥。有人指出，TPM 2.0 可以加密痕迹上的磁盘加密密钥，使这种攻击成为不可能。](https://hackaday.com/2021/07/30/this-week-in-security-fail2rce-tpm-sniffing-fishy-leaks-and-decompiling/)

整个可信计算模型的前提是 CPU 本身是可信的。这又让我们回到了英特尔的公告，即可以通过物理访问启用调试模式。在这种调试模式下，可以提取 CPU 主密钥，从而导致完全破坏。可以恢复驱动器加密密钥，并且可以将未签名的固件加载到管理引擎中。这意味着 TPM enclave 中的数据和 TPM 存储的加密密钥可能会受到威胁。主板供应商正在推出更新的固件来解决这个问题。

## 通过 ICMP 的 DNS 中毒

为了纪念已故的丹·卡明斯基，[我们再次关注 DNS 缓存中毒](https://arstechnica.com/gadgets/2021/11/dan-kaminskys-dns-cache-poisoning-attack-is-back-from-the-dead-again/)。这一次是 Linux 网络栈的一个怪癖使得攻击成为可能。来自加州大学河滨分校的三人组在[的一篇论文中详细描述了这次攻击。](https://www.cs.ucr.edu/~zhiyunq/pub/ccs21_dns_poisoning.pdf)

最初的 DNS 攻击使用非随机查询 id，并且总是从 UDP 端口 53 进行 DNS 查找。发送伪造的 DNS 响应很简单，如果恶意响应在有效响应之前到达，解析器就会接受伪造的数据。使这种攻击特别糟糕的是解析器缓存这些结果，所以许多用户可以被发送伪造的数据。解决方案是随机化源端口(16 位)和事务 ID (16 位)。这两种保护都没有包含足够的安全位，但组合起来的空间足以使 DNS 攻击变得不切实际。如果这些值中的一个可以被独立地确定，攻击可能再次有效。

这种攻击滥用了 ICMP 碎片错误。当 Linux 机器接收到这样的消息时，它会根据活动的 UDP 连接进行验证。该请求必须包含正确的源和目的 IP 和端口。如果这组信息与一个打开的 UDP 套接字匹配，则在异常缓存中添加一个条目。如果攻击者能够检测到异常缓存的状态变化，他可以使用 ICMP 数据包来探测打开的 UDP 套接字，从而有效地允许发现 DNS 查找的随机端口。

您如何准确地检测到状态变化？像`dnsmasq`这样的 DNS 解析器使用`sendto()`打开这些临时端口，这具有接受来自任何 IP 地址的 UDP 包的无意副作用。ICMP 碎片错误可以更新任何 IP 的异常缓存，只要它具有临时连接的正确 IP 和端口。这使得攻击变得微不足道。

向`somerandomsubdomain.google.com`发出请求，然后开始向目标系统上的所有 UDP 端口发送 ICMP 碎片错误。当这些数据包中的一个与打开的 UDP 端口匹配时，指定 IP 的 MTU 将被更改。然后从 ICMP 错误中指示的 ping 系统。当您的一个 ping 响应出现碎片时，您就发现了冲突。既然您已经知道了 DNS 解析器打开的端口，那么您就可以暴力破解事务 ID。因为它只有 16 位的密钥空间，这是非常可行的。

对于其他 DNS 解析器，比如 BIND，这个问题有点难，它们使用`connect()`来打开临时 UDP 套接字。同样的技巧也适用，但是您只能在套接字连接的特定 IP 上触发 MTU 更改。有什么办法能察觉到这种变化吗？有。这里的关键是异常缓存是一个深度有限的哈希表。这个哈希表通过对远程 IP 地址应用一种算法(哈希)来工作，它总是返回一个 11 位的数字。分配了 2048 个内存“桶”,哈希得到的数字决定了异常数据进入的桶。每个存储桶可以包含五个条目，当第六个异常存储在该存储桶中时，最旧的将被丢弃。

在这种情况下，攻击者需要控制与实际上游解析器的哈希值发生冲突的远程 IP。攻击者填充其冲突 IP 的五个异常条目，然后发起 ICMP 碎片错误风暴。攻击者可以测试他控制的 IP 的 MTU，因此将知道他的一个异常何时被丢弃。这表明他已经为临时 UDP 连接找到了正确的端口。

这是一个复杂的攻击，但潜在的回报是相当高的，所以期待在不久的将来看到解决这个问题的补丁。

## 将 KB 编号武器化

Microsoft 使用知识库文章编号跟踪他们的安全更新。例如，CVE-2021-42279 被微软追踪为用于 Windows 10 64 位的 KB5007207。列出已经安装在 Windows 系统上的知识库是很容易的，但是如何将它转化为潜在漏洞的列表呢？[【阿里斯·惠根】有答案](https://bitsadm.in/blog/windows-security-updates-for-hackers)。有很多工具可以查询已安装的知识库列表，其中许多工具甚至可以在远程系统上工作，比如`systeminfo.exe`和`WMIC.exe`。所以对于你所有的 Windows 开发需求，你只需要看看[的 Windows 开发建议者——下一代](https://github.com/bitsadmin/wesng)。这个工具集看起来像是一个用于审计或红队 Windows 机器的有用工具包，所以一定要把它添加到你的玩具盒中。

## 有一次联邦调查局发了垃圾邮件

你知道怎么处理垃圾邮件吧？如果一封邮件看起来可疑，它就会被放入垃圾邮件文件夹，再也不用担心了。因此，当一封来自 FBI 的邮件到达时，你只是嗤之以鼻，迅速检查邮件标题以确保无误，然后就离开了。但是等等，那封邮件来自`153.31.119.142`，实际上是`mx-east-ic.fbi.gov`。这是怎么回事？

> 这些邮件看起来像这样:
> 
> 发送 IP:153.31.119.142([https://t.co/En06mMbR88](https://t.co/En06mMbR88))
> 发件人:eims@ic.fbi.gov
> 主题:紧急:系统中的威胁者[pic.twitter.com/NuojpnWNLh](https://t.co/NuojpnWNLh)
> 
> —Spamhaus(@ Spamhaus)[2021 年 11 月 13 日](https://twitter.com/spamhaus/status/1459452609979371520?ref_src=twsrc%5Etfw)