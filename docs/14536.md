# 本周安全:安全引导旁路，攻击泰坦 M，KASLR 弱点

> 原文：<https://hackaday.com/2022/08/19/this-week-in-security-secure-boot-bypass-attack-on-titan-m-kaslr-weakness/>

对于最终用户来说，安全引导到底有多有用还存在争议，但现在安全引导又出现了另一个问题，或者更具体地说，是三个签名的引导加载程序。Eclypsium 的研究人员已经发现了 Eurosoft、CryptoPro 和 New Horizon 引导加载程序中的问题。在前两种情况下，过于灵活的 UEFI shell 允许原始内存访问。一个启动脚本不需要签名，可以很容易地随意操纵引导过程。最后一个问题是在新的 Horizon Datasys 产品中，该产品在启动过程的其余部分禁用任何签名检查，同时仍然报告安全启动已启用。目前还不清楚这是否需要一个配置选项，或者只是默认完全中断。

真正的问题是，如果恶意软件或攻击者可以获得对 EFI 分区的写访问权限，这些签名的引导加载程序之一可以与一些讨厌的有效负载一起添加到引导链中，最终引导的操作系统仍然可以看到安全引导。它是真正隐形感染的完美载体，类似于我们几周前报道的恶意固件[。
](https://hackaday.com/2022/07/29/this-week-in-security-symbiote-smart-locks-and-cosmicstrand/)

## 赌博？

网上赌博。就像在赌场赌博一样，从设计上来说，赌场几乎总是赢家。但也像一个真正的赌场，有一些聪明的技术，如在 21 点算牌，这就足以把赔率变成对你有利。在这种情况下，你会记录已经打出了多少张大小牌，并相应地调整你的赌注。 [NCC 集团调查了一个“六大”在线赌场游戏](https://research.nccgroup.com/2022/08/16/wheel-of-fortune-outcome-prediction-taking-the-luck-out-of-gambling/)——这个游戏与大多数在线赌博有点不同，因为有一个真人担任赌台管理员。赌台管理员转动决定下注结果的轮盘。人类和计算机有一些共同点，因为我们都天生不擅长产生好的随机性。

他们从收集数据开始，然后对数据进行分析，找出值得注意的模式。对 7000 多轮游戏进行了分析，发现了赌博结束前轮盘的位置与中奖号码之间的相关性。简而言之，赌台管理员倾向于每次都用相同的力旋转轮盘。一点计算机视觉和脚本赌博，他们有一个赢的组合。赢了多少？1000 轮后投资回报率略高于 20%。

## 进击的巨人

Quarkslab 的团队对 Titan M(谷歌在 Pixel 手机上的安全芯片)有点着迷。在它的其他功能中，泰坦为秘密提供了一个安全的飞地。它通过 SPI 与手机的主处理器进行通信，并具有所有预期的安全功能和缓解措施来保护秘密的安全。嗯，几乎所有的。这种专用处理器的简单设计也意味着它没有更复杂的处理器可能有的任何复杂的内存损坏保护。这也很简单，内存布局是静态的。

Quarkslab 的第一次攻击是使用他们的[no client](https://github.com/quarkslab/titanm/tree/master/nugget_toolkit/)向泰坦发送任意消息——黑盒模糊化。把这想象成把各种尺寸的意大利面条扔向虚拟墙，看看是否有面条，或者更确切地说是碰撞。这绝对是一项有价值的技术，有时这是所有可用的技术，但是您通常无法通过这种方式找到更有趣的代码路径。这些家伙真的知道他们的方式围绕泰坦 M，所以去了一个不同的方法，仿真固件的一部分，并模糊了仿真设备。这很难实现，并且存在一些限制，因为您的仿真通常不会与真实的硬件完美匹配，但好处是您可以获得代码路径，这些路径仅通过模糊化是很难随机到达的。

找到他们做的一个 bug。通过发送一个`ImportKeyRequest`，一个`0x01`可以被写入一个不完全任意的越界位置。通过在请求中包含多个标签，可以一下子完成多次。这是一个非常有限但坚实的开始。关键是覆盖一个由不同的程序使用的指针，即 Keymaster 请求处理器。指针指向传入请求将被复制到的位置，因此攻击开始成形。使用单字节原语毒害 keymaster，然后发送一个请求，该请求被写入这个新位置。通过实验，他们发现可以发送 556 个任意字节，后跟一个内存地址，执行将跳转到该地址。这需要一点时间，但通过一些面向返回的编程，这足以从芯片上的任何地方读取存储器，并通过 SPI 总线将其发送回客户。谷歌 6 月份的安全综述包括对这个非常聪明的漏洞的修复。

## MacOS 上的 KASLR 旁路

泰坦 M 中缺少的缓解措施之一是内核[地址空间布局随机化](https://en.wikipedia.org/wiki/Address_space_layout_randomization)，但是 KASLR 在 MacOS 中相当普遍，使得内核级利用更加难以实现。或者应该是，除了在 MacOS KASLR 上设计了一个相当大的[洞](https://blog.ret2.io/2022/08/17/macos-dblmap-kernel-exploitation/)。这个特征就是冬眠，或者更准确地说，从冬眠中醒来。有一个`__HIB`内核段总是被映射到同一个地址，并作为唤醒的一部分被调用。这个段的一部分是`dblmap`内存块，它实际上被映射到虚拟内存空间两次。它在用户空间/内核空间上下文切换中使用。由于它在用户模式下的可用性，它很容易受到彻底的攻击，并且那里的指针泄露了“slide”值 KASLR 基址。即使在防熔毁的 CPU 上，`__HIB`扇区也有一些其他用途。帖子里还有很多，而且不太可能很快修复，所以如果 MacOS 漏洞是你的事，玩得开心点！

## 什么？WTFIS？

如果 XNU hacking 超出了你的工资级别，就像我的，那么这个工具可能更适合我们的速度。`wftis`是一个来自多个来源的新工具，[就像是`whois`的迭代](https://github.com/pirxthepilot/wtfis)。它从 Virustotal、Passivetotal 和 IPWhois 中提取信息，以获取给定域名的数据。如果一个奇怪的域出现在你的日志中，wtfis 可能是你可以求助的工具。对于前两个服务，它确实需要 API 密钥，但是在它们的自由层上应该工作得很好。
[![](img/00b26ed283822b22bbd717688d2a6660.png)](https://hackaday.com/wp-content/uploads/2022/08/demo.gif)

## 声波攻击

最后，我最近遇到的最奇怪的网络传说。非常感谢 Discord 上的[mtxyz]指出了 [CVE-2022-38392](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2022-38392) ，一个刚刚曝光的[老问题。](https://devblogs.microsoft.com/oldnewthing/20220816-00/?p=106994)一家笔记本电脑 OEM 发现节奏之国的音乐视频确实会导致他们的笔记本电脑崩溃。更奇怪的是，在一台笔记本电脑上播放这首歌也会让附近的笔记本电脑崩溃。最终发现，这些笔记本电脑中的 5400 RPM 硬盘驱动器有一个由这首歌激发的共振频率，导致了暂时的故障。解决方案是使用硬编码频率滤波器来提取该频率。听起来有点像对着数据中心的硬盘大喊大叫。享受:

 [https://www.youtube.com/embed/tDacjrSCeq4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/tDacjrSCeq4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

