# 本周安全:Imagemagick、Solarwinds 和 DHCP 诡计中的 Ghoscript

> 原文：<https://hackaday.com/2021/09/10/this-week-in-security-ghoscript-in-imagemagick-solarwinds-and-dhcp-shenanigans/>

针对 Ghostscript 解释器中的一个潜在严重缺陷，刚刚发布了一个 PoC。Ghostscript 可以加载 Postscript、PDF 和 SVG，并且它有一个来自 Postscript 的特性，这是一个持续的安全问题:`%pipe%`命令。这个命令请求解释器产生一个新的进程——它是规范中的 RCE。对于不受信任的图像和文档来说，这显然是一个问题，Ghostscript 在过去几年中多次修复了这个错误功能的安全漏洞。

这个特殊的漏洞[是由【埃米尔·勒纳】](https://twitter.com/emil_lerner/status/1430502815181463559)发现的，并在 ZeroNights X. [上进行了描述，talk 在](https://www.youtube.com/watch?v=BQVoHLfAc8A)上可用，但用的是俄语。这个问题似乎是某种绕过，其中管道命令似乎在`/tmp/`目录中工作，但是一个简单的分号允许执行任意命令。为什么这是一件大事？因为 ImageMagick 在某些发行版上默认使用 Ghostscript 打开 SVG 图像，并且 ImageMagick 经常用于自动调整大小和转换网站的图像。在[Emil]的演示中，他将这一缺陷作为针对三家不同公司的攻击链的一部分。

我无法重现我的 Fedora 安装上的缺陷，但我也没有发现它在 Ghostscript 或 Imagemagick 变更日志中被修复的任何通知。目前还不清楚这个问题是否已经被修复，或者这是否是一些平台的真正 0 天。无论哪种方式，预计攻击者会开始尝试利用它。

### SIP 客户端被削减

[CVE-2021-33056](https://claroty.com/2021/08/31/blog-research-crashing-sip-clients-with-a-single-slash/) 是 Linphone SIP 客户端解析 SIP 报头的一个奇怪的错误。SIP 数据包中的多个报头字段需要是有效的 URIs，并且应该是 SIP URIs —类似于`sip:alice@example.com`。问题是，什么是有效的 URI 有很大的灵活性。在这种情况下，单斜线“/”是有效的 URI。该代码试图提取方案，如果没有找到，则返回一个空指针。然后，该指针未经验证就被传递给下一个函数，从而导致崩溃。空指针引用很难转变成简单的 DoS 攻击，这似乎也不例外。这里最大的挑战是，Linphone 堆栈已经进入了各种移动和物联网客户端。

### 又是太阳风

在过去的几周里，Solarwinds 设备遭受了另一次 0 日攻击，这次是针对 SSH 服务的。来自微软的研究人员确定，主要攻击者是来自中国的 APT，并能够重现攻击。主要问题？Solarwinds 推出了自己的 SSH 服务器，而不是使用 OpenSSH 这样的成熟解决方案。该服务关闭了地址空间布局随机化，并发现了一个奇怪的行为。当运行模糊化工具并用调试器观察进程时，微软研究人员观察到多个应该会使进程崩溃的异常。相反，异常被记录下来，试图清除损坏，过程继续进行。虽然发现并修复了一条成功的 RCE 链，但不能确定这就是在野外使用的那条链。如果不对该服务进行重大更改，它应该仍然是易受攻击的。

### DHCP 技巧

如果攻击者控制了发送到路由器的 DHCP 响应，会造成什么样的麻烦？除了路由之外，这显然取决于路由器提供什么服务。Anvil Secure 的研究人员使用术语“智能路由器”，这意味着一种设备可以做一些事情，如服务文件、托管 VPN 或管理 IP 摄像头。在这种情况下，当 IP 范围发生冲突时，会发现一些奇怪的边缘情况。

简而言之，您可以使用更具体的 DHCP 范围将内部 IP 路由到路由器 WAN 端的攻击者。这可能被用来设置 MitM 攻击，并拦截文件传输或 VPN 流量。虽然这很有趣，但这种攻击并不适用于整个网络，因此影响有限。这可能是由已接管调制解调器或路由器和调制解调器之间附加硬件的攻击者完成的。

### 溢出使走私成为可能

本周发布了另一个请求走私的巧妙方法，这个[是 HAProxy](https://jfrog.com/blog/critical-vulnerability-in-haproxy-cve-2021-40346-integer-overflow-enables-http-smuggling/) 中的一个漏洞。CVE-2021-40346 是一个整数溢出，由恶意标题触发:`Content-Length0aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa...:`实际攻击有超过 240 个“a”字符，使总字符数达到 270。该头名称存储在一个数据结构中，该数据结构使用一个 8 位整数来跟踪字符串长度。由于 270 大于最大值 256，该值溢出并被视为长度 14，这恰好是看起来有效的`Content-Length`的长度。恰好这个数据结构中的下一个字段是值的长度(冒号后的部分)。溢出将该值设置为 1。虽然这些都作为一个可能的头存储，但下一行实际上是一个有效的内容长度头，并立即被接受，导致消息的其余部分被读入内存。

`POST /index.html HTTP/1.1
Host: abc.com
Content-Length0aaaa...:
Content-Length: 60`

GET/admin/add _ user . py HTTP/1.1
主持人:abc.com
ABC:XYZ

既然数据包已经加载到内存中，下一个处理阶段就将它写入发送到后端的数据包中。在这里，明显无效的报头基于被操纵的长度值被处理，导致在输出分组上设置一个`Content-Length: 0`报头。其余的数据随后被附加到同一个数据包中，这就是现在被走私的请求。一旦后端接收到这个数据包，content-length 报头就意味着在同一个数据包中发送两个单独的消息。因此，第二个请求已经偷偷通过了前端服务器上的安全控制。

### OpenWRT 版本

OpenWRT】刚刚发布了 2021.02.0 ，这是一个基于 5.4.143 LTS 内核的新的主要版本。有一些值得注意的新安全特性，包括默认的 WPA3 和 SSL 支持，以及二进制文件的 ASLR。现在还支持运行 SELinux，尽管默认情况下这不是开启的。随着新功能的出现，由于更高的系统要求，许多旧设备不再受到官方支持。现在，8 MB 闪存和 64mb ram 是完全支持所需的最低容量。