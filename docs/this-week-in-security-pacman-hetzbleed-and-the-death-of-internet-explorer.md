# 本周安全:吃豆人，赫茨布莱德，和互联网浏览器的死亡

> 原文：<https://hackaday.com/2022/06/17/this-week-in-security-pacman-hetzbleed-and-the-death-of-internet-explorer/>

本周要讨论的不是一个，而是两个旁道攻击。首先出场的是 [Pacman](https://pacmanattack.com/) ，绕过 ARM 的指针验证码。PAC 是内置于某些 ARM 处理器中的一种保护措施，当更新指针时，必须正确设置加密哈希值。如果散列设置不正确，程序就会崩溃。其思想是，大多数利用使用指针操作来实现代码执行，正确设置 PAC 需要显式的指令调用。PAC 实际上是在指针本身的未使用位中指示的。AArch64 架构使用 64 位值进行寻址，但地址空间远小于 64 位，通常为 53 位或更少。这为 PAC 值留下了 11 位。请记住，应用程序不保存键，也不计算这个值。11 位似乎不足以保证安全，但请记住，每次尝试失败都会导致程序崩溃，每次应用程序重启都会重新生成密钥。

Pacman 引入的是 oracle，这是一种深入了解攻击者不应看到的数据的方法。在这种情况下，先知通过推测攻击工作，非常类似于 Meltdown 和 Spectre。关键是尝试推测性地取消对受保护指针的引用，然后观察系统状态的变化。您可能会注意到，这需要攻击者已经在目标系统上运行代码，才能运行 PAC oracle 技术。Pacman 不是一个远程代码执行缺陷，也不能用于获得 RCE。

更重要的一点是，为了从这种保护中受益，应用程序必须编译 PAC 支持。广泛使用 PAC 的平台是 MacOS，因为它是 M1 处理器中的一个特性。攻击链可能从缺少 PAC 支持的应用程序中的远程执行错误开始。一旦在 uprivileged 用户空间中建立了立足点，Pacman 将被用作针对内核的漏洞利用的一部分。详见[PDF 文件](https://pacmanattack.com/paper.pdf)。

### 心脏出血

[![](img/3c2fbf593c4bfd5fe075d49565c9d3d4.png)](https://hackaday.com/wp-content/uploads/2022/06/Hertzbleed-logo-with-text.png)

另一种旁道技术是对旧思想的新尝试。 [Hertzbleed](https://www.hertzbleed.com/) 基于这样的想法，即有可能检测到运行在基本频率的 CPU 和运行在增强频率的 CPU 之间的差异。这两种状态之间的差异实际上可以泄露一些关于 CPU 正在做什么的信息。这里有[他们论文的预发布 PDF](https://www.hertzbleed.com/hertzbleed.pdf) 以查看细节。最大的结果是，针对计时攻击的标准防护措施(常数时间编程)并不总是可靠的安全措施。

它之所以有效，是因为最大频率取决于处理器散热设计功率(TDP)，即 CPU 设计使用的最大功率和散热量。不同的指令实际上会使用不同量的功率，并基于此产生或多或少的热量。更多的热量意味着更早的节流。并且可以在响应时间中检测到节流。这其中的细节相当引人入胜。您知道吗？即使运行相同的指令，寄存器值不同，功耗也会略有不同。他们选择了一种单一的加密算法，SIKE，一种量子安全的密钥交换技术，并试图通过定时攻击提取服务器的密钥。

在这项研究中，SIKE 也发现并揭示了一个怪癖，即有可能缩短算法的一部分，这样一系列内部的中间步骤会导致零值。如果您知道静态密钥的多个连续位，就有可能构造一个挑战来解决这个问题。推而广之，你可以猜测下一个未知位，只有猜对了才会陷入怪圈。SIKE 使用常数时间编程，所以这种奇怪的行为应该没什么关系。这里赫茨布莱德观察因素。当运行包含这种级联零行为时，SIKE 算法消耗更少的功率。消耗更少的功率意味着处理器可以更长时间地保持全加速时钟，这意味着密钥交换完成得稍微更快。甚至可以通过网络连接检测到它。他们对 Cloudflare 的 CIRCL 库和微软的 PQCrypto-SIDH 进行了测试，并能够分别在 36 小时和 89 小时内从两种实现中恢复密钥。

有一种针对这一特定缺陷的缓解措施，可以检测到可能触发级联零的挑战值，并在任何处理发生之前阻止该值。看看其他算法中的怪癖是否能被发现并使用同样的技术武器化，这将是一件有趣的事情。不幸的是，在处理器方面，唯一真正的缓解措施是完全禁用升压时钟，这对处理器性能有很大的负面影响。

### 击败 Nest 安全引导

[Frédéric Basse]有一个 Google Nest Hub，[他非常想在上面运行自己的 Linux 发行版](https://fredericb.info/2022/06/breaking-secure-boot-on-google-nest-hub-2nd-gen-to-run-ubuntu.html)。不过，有一个问题。Nest 使用安全引导，没有官方方法解锁引导程序。从什么时候开始一个专注的黑客会让这阻止他？第一步是找到一个 UART 接口，隐藏在带状电缆的一些未端接通道上。一个定制的分线板，他有一个 U-Boot 日志。下一步是运行启动按钮组合，并查看 U-Boot 试图用每个按钮做什么。其中一种组合允许从 recovery.img 引导，如果不是为了安全引导，这将是理想的。

U-Boot 的伟大之处在于它在 GPL 下是开源的，这意味着源代码应该可供阅读。在源代码中找到一个错误，就可以绕过安全引导。开源也允许一些有趣的方法，比如在用户空间运行部分 U-Boot 代码，并用 fuzzer 来练习。这种方法发现了一个错误，大于 512 字节的块大小会触发缓冲区溢出。这通常是一个安全的假设，因为实际上没有块大小大于 512 的 USB 存储设备。

不要担心，像 Raspberry Pi Pico 这样的设备可以运行 TinyUSB，它允许用您指定的任何块大小来模拟 USB 设备。一项测试表明，这种方法确实会在真实设备上导致可重复的崩溃。代码执行相当简单，编写一堆指令，本质上是指向有效负载的`noop`代码，然后覆盖返回指针。在 can 中执行代码，剩下的就是覆盖命令列表并执行自定义的 U-Boot 脚本。美好的事物。

### 砰

卑微的`ping`命令。一对数据包能告诉我们关于网络和远程主机的多少信息？[据【高清摩尔】，颇有点](https://www.rumble.run/blog/lean-network-discovery-icmp/)。例如，以 ping 响应的给定时间为例，根据每毫秒 186 英里计算距离。这是主机的绝对最大距离，尽管该距离的四分之一和一半是距离估计的合理下限和上限。TTL 很可能从 64、128 或 255 开始，您可以猜猜沿途遇到的跳数。哦，如果这个响应是从 64 开始的，那么它很可能是 Linux 机器，128 表示 Windows，255 通常表示 BSD 派生的 OS。

收到“目的主机不可达”消息本身就很有趣，它会告诉您应该能够到达给定 IP 的路由器。然后是广播 IP，它将消息发送给子网中的每个 IP。使用 Wireshark 之类的工具进行数据包捕获在这里很有启发性。命令本身可能只显示一个响应，即使多个设备可能已经响应。这些响应中的每一个都有一个 MAC 地址，可以通过查找来确定供应商。另一个有趣的技巧是欺骗 ping 数据包的源 IP 地址，使用您用公共 IP 地址控制的机器。Ping 网络上的每台设备，许多设备都会通过默认网关发送响应。您可能会发现不应该存在的互联网连接或 VPN。谁知道你能从卑微的人身上学到这么多。

### 比特和字节

Internet Explorer 真的死了。如果你和我一样，认为 Internet Explorer 几年前就已经退役了，那么当你知道它在过去的一周里终于退役了，你可能会感到惊讶。本月的补丁星期二是 IE 得到官方支持的最后一天，从现在开始它完全不受支持，并且预计最终会自动从 Windows 10 机器上卸载。同样在这个月发布的补丁还有[最终修复了 Follina](https://blog.malwarebytes.com/exploits-and-vulnerabilities/2022/06/update-now-microsoft-patches-follina-and-many-other-security-updates/) ，以及其他一些重要的修复。

上周，HTTPS DDOS 攻击创下新纪录: [Cloudflare 缓解了由每秒 2600 万次请求组成的攻击](https://blog.cloudflare.com/26m-rps-ddos/)。HTTPS 攻击是由原始数据饱和以及服务器资源耗尽组成的组合拳。攻击来自虚拟机和服务器组成的僵尸网络，其中最大一部分来自印度尼西亚。

运行 Travis CI 的免费层？您知道吗[全世界都可以通过 Travis API 调用](https://blog.aquasec.com/travis-ci-security)访问您的日志？最重要的是，自 2013 年以来的所有跑步记录似乎都可用。可能是时候撤销一些访问密钥了。Travis 试图审查访问令牌，但不管怎样，还是有相当多的令牌通过了筛选。

想知道 TPM 密钥嗅探在启动时的风险矩阵是什么样的吗？[不好看](https://www.secura.com/blog/tpm-sniffing-attacks-against-non-bitlocker-targets)。Secura 的研究人员研究了六个流行的加密和安全引导应用程序，没有一个使用参数加密功能来加密网络上的密钥。讽刺的结论？分立的 TPM 芯片不如内置在主板固件中的安全。