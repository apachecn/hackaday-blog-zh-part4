# 本周安全:ISNs、补丁星期二和俱乐部会所

> 原文：<https://hackaday.com/2021/02/19/this-week-in-security-isns-patch-tuesday-and-clubhouse/>

先说 TCP。具体来说，不同的 TCP 连接如何保持不同，第三方如何防止中断连接？帮助完成这一壮举的机制之一是 TCP 序列号。TCP 连接的两个端点中的每一个都跟踪一个递增的 32 位数字，对应于连接中发送的字节。这很方便，因为每一方都可以使用该值来跟踪他们收到了数据流的哪一部分。例如，对于丢失的分组，可以发送消息请求重发字节 7-15。

连接的每一端都设置自己的初始序列号(ISN ),这个序列号必须是唯一的，因为冲突会导致流混淆。这句话应该会让你的安全蜘蛛感觉刺痛。如果偶然发生的碰撞会导致问题，那么黑客可以故意用它做什么呢？很有可能。知道了当前的序列号，以及其他一些信息，第三方可以关闭 TCP 流，甚至注入数据。这种攻击已经存在多年，最初被称为[米特尼克攻击](http://wiki.cas.mcmaster.ca/index.php/The_Mitnick_attack)。这最初是可能的，因为 TCP 实现使用一个简单的计数器来设置 ISN。一旦理解了这种方法的安全后果，主要的实现就转向为他们的 ISNs 生成随机数。

现在来看本周的故事:[fores cout 的研究人员花时间检查了 11 个 TCP/IP 堆栈](https://www.forescout.com/company/blog/numberjack-forescout-research-labs-finds-nine-isn-generation-vulnerabilities-affecting-tcpip-stacks/)的漏洞，以防范旧的 Mitnick 攻击( [PDF 白皮书](https://www.forescout.com/company/resources/numberjack-weak-isn-generation-in-embedded-tcpip-stacks/))。在发送的 11 个嵌入式堆栈中，有 9 个在其 ISN 一代中有严重的弱点。大多数易受攻击的实现使用系统时间值作为其 ISN，而有几个使用可预测的伪随机算法，可以很容易地逆转。

简历已经分配好了，供应商也收到了“编号:JACK”的通知，这是 Forescout 的研究名称。大多数易受攻击的软件已经有可用的补丁。嵌入式系统的问题在于，它们通常不会获得安全更新。易受攻击的网络堆栈存在于 IP 摄像头、打印机和其他“不可见”软件等设备中。时间会证明这种攻击是否会成为未来物联网僵尸网络的一部分。

### 微软补丁星期二

上周，微软发布了他们的月度补丁综述，其中有一些有趣的 bug。 [CVE-2021-24074](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-24074) 是对源路由数据包处理不当导致的潜在 RCE。“源路由”是最容易被遗忘的 IP 选项之一，尽管它在利基应用中确实有一些用途。使用此选项的数据包通常会被路由器和安全设备阻止，这使得通过公共互联网发送此类数据包基本上是不可能的。Windows 客户端也会阻止这些数据包，但在阻止此类数据包时会生成 ICMP 响应。从字里行间来看，该漏洞似乎是由构建 ICMP 响应的过程触发的。([不是新问题](https://hackaday.com/2018/11/01/apple-kernel-code-vulnerability-affects-everything/))补丁是可用的，这是一个简单的解决方法:简单地丢弃没有响应的输入包。

另外两个简历可能值得注意，尽管关于它们的信息更少。 [CVE-2021-24078](https://msrc.microsoft.com/update-guide/en-US/vulnerability/CVE-2021-24078) 是 Windows DNS 服务器中的一个蠕虫漏洞。幸运的是，服务器只有在 DNS 组件打开的情况下才容易受到攻击。另一个是 [CVE-2021-26701](https://msrc.microsoft.com/update-guide/en-US/vulnerability/CVE-2021-26701) ，一个比较模糊的”。NET Core 远程代码执行漏洞”。它的严重等级为“严重”,微软已经表示详细情况已经公开。

### 会所安全成长的烦恼

你可能听说过 Clubhouse 是新的社交媒体昙花一现。或者，也许它会留下来，谁知道呢。如果你还没有深入了解，Clubhouse 有点像一个音频聊天室，名人或老师可以在这里与观众进行对话。现在还是发布前，已经有 800 万次下载了。正如你可能想象的那样，这一成功让 Clubhouse 进入了安全研究人员的视线，就像 Zerforschung 的那些人一样。看起来 Clubhouse 是建立在 Agora.io 平台上的，这里的攻击是直接和 Agora.io 对话而不是通过 Clubhouse app。结果呢？攻击者可以离开房间，但保持与后端的连接。用户名消失了，但仍然可以接收音频，甚至可以对着房间说话。这破坏了将房间设置为单扬声器模式的能力，并使驱逐用户成为不可能。

### 电报自毁信息

问题？它们实际上并没有被析构。【Dhiraj Mishra】对 MacOS 版本的 Telegram 进行了研究，发现在自毁消息中发送的音频和视频文件仍然可以在计算机硬盘上使用，即使在消息计时器过期之后。对于额外密码，在某些情况下，这个版本的电报也以明文形式存储密码。这两个问题都已修复，所以如果你在 MacOS 上使用 Telegram，请确保进行更新。

### 更多的 NPM 依赖困惑

上周我们报道了[Alex Birsan]的依赖混淆攻击，在这种攻击中，一个包可以使用私有包的名称上传到 NPM。如果一个公司的构建系统配置错误，公共包可以被拉进最终的构建中，而不是预期的私有包。自从[Alex]公开宣布攻击以来，[将近 300 个这样的包利用这种技术被上传到 NPM](https://www.bleepingcomputer.com/news/security/copycats-imitate-novel-supply-chain-attack-that-hit-tech-giants/)。请注意，这些都是已经发现的包，几乎可以肯定还有更多包在外面，但是还没有被发现。[Alex]指出，其中一些可能是其他旨在获得 bug 奖金的研究人员，但其中甚至可能有一些合法的恶意软件包。

我们将尽最大努力让您了解这些故事的最新进展，以及每周出现的其他内容，敬请关注！