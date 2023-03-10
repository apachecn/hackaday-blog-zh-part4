# 本周在安全方面:PHP 攻击化解，记分牌操纵，和 Tillitis

> 原文：<https://hackaday.com/2022/10/07/this-week-in-security-php-attack-defused-scoreboard-manipulation-and-tillitis/>

如果您使用 PHP，您可能会使用 Composer 工具来管理依赖项，至少是间接的。SonarSource [的优秀人员在这个工具中发现了一个令人讨厌的、潜在的供应链攻击](https://blog.sonarsource.com/securing-developer-tools-a-new-supply-chain-attack-on-php/)，当它被用于 Packagist 仓库时。问题是对任意自述文件名的支持。当 Packagist 上出现软件包更新时，该服务使用版本控制服务(VCS ),如 Git 或 Mercurial，来获取指定的 readme 位置。该拉操作受参数注入的影响。将您的分支命名为`--help`，Git 将很乐意运行 help 参数，而不是执行 pull。在 Git 命令的情况下，我们勇敢的研究人员无法将问题武器化以实现代码执行。

Composer 还支持使用 Mercurial 作为 VCS 的项目，Mercurial 有一个`--config`选项，它具有…有趣的潜力。它允许将一个 Mecurial 命令重新定义为一个脚本片段。所以一个项目只需要包含一个恶意的`payload.sh`，并且 readme 设置为`--config=alias.cat=!hg cat -r : payload.sh|sh;,txt`。对于那些在家跟踪的人来说，漏洞在于 Composer 接受这个被诅咒的字符串 ugly 作为有效的文件名。这使用了`--config`技巧将`cat`重新定义为一个执行有效负载的脚本。它以`.txt`结尾，因为这是作曲家的要求。

因此，让我们来谈谈这个小黑客可能被用来做什么，或者可能仍然被用来在一个未打补丁的，私人安装的 Packagist 上。这是一种无人值守的攻击，直接跳转到远程脚本执行—在官方软件包存储库上。如果被发现并用于邪恶目的，这将是针对 PHP 部署的大规模供应链攻击。相反，多亏了 SonarSource，它在 4 月份被发现并被私下披露。Packagist 的官方 Packagist 回购在披露后的第二天就被修复了，而 CVE 和更新的软件包在六天后才发布。到处都是伟大的作品。

## 记分员的优势

[麦克斯韦·杜林]又名[三振出局]正在观看一场高中篮球比赛，[突然注意到无线记分牌控制器](https://maxwelldulin.com/BlogPost/Scoreboard-Hacking-Signal-Analysis-Part-1)。如果他能改变比分呢？会有多难呢？你可能知道这是怎么回事。他已经被[书呆子狙击](https://xkcd.com/356/)。他为此花了几个月的时间，甚至在这个过程中拿到了火腿执照。结论呢？比你想象的更有挑战性。

这个黑客攻击的第一部分从阅读无线电芯片上的文档开始，然后进行一些真实的捕获和数据分析。关于那些数据。发送内容的一个小变化导致空中数据的巨大变化。达到一次改变 128 位的程度。这个简单的小记分牌系统被加密了！AES-128 加密保护系统不被随意篡改。但是我们的英雄不仅仅是一个随意的篡改者。

[![](img/4219dc81c74c330ba65d0042908a095d.png)](https://hackaday.com/wp-content/uploads/2022/10/ScoreboardBaseState.jpg) 遂，[下篇](https://maxwelldulin.com/BlogPost/Scoreboard-Hacking-Part-2)。接下来是再次查看硬件，并绘制 PCB 走线。发射器是连接到 HopeRF 收发器的 ATmega。接收器是一个匹配的收发器和 ATMega，连接到一个通过 HDMI 处理记分牌显示的 Raspberry Pi 3 A+。Raspberry Pi 是一个很好的开始，它既有 SD 卡可供研究，又有 USB 端口中的 USB 驱动器。ATmega 板上最令人感兴趣的是串行端口和基于串行的调试端口。大量潜在的攻击面。调查 Pi 的固件确实取得了重大胜利。解码无线数据包的软件是用 C#编写的，可以使用 [DNSpy](https://github.com/dnSpy/dnSpy) 进行反编译。虽然这是很大的一步，但是需要注意的是加密密钥本身。

是时候焊接到 ATmega 上了，看看是否会泄露它的秘密。前面提到的调试接口 ICSP 有一个命令，可以读取整个芯片的内存。完美！因为不可能那么容易，芯片的安全设置被启用，这禁止了该命令。传统的串行端口方法同样失败，因为走线在生产板上接地。还有一个接口需要考虑，即 ATmega 与收发器之间的串行外设接口(SPI)连接。系统引导期间通过该链路发送什么数据？原来，RF 模块在该系统中承担着加密的重任，这些模块在断电时会完全丢失其配置。嗅探密钥导致轻松获胜，并且密钥值为`0x01020304050607080102030405060708`。这可能不是一个随机值。

第三部分带着这个重要的发现，进入实际发送无线数据包的领域。然而，航行并不容易，因为有“数据白化”需要处理。这个奇怪的术语只是指时钟漂移问题，即在一个无时钟信号上连续发送太多的“0”或“1”。白化使用线性反馈移位寄存器(LFSR)算法，一旦你算出了那个数学，你就缺少初始值了。幸运的是，每个数据包都发送了一些白化的数据，而不是加密的数据——这种算法只有 511 种可能的初始状态，因此找到正确的 IV 并不困难。看起来真正的挑战是找出循环冗余校验(CRC)。这些是非加密的错误检查例程，它们存在于许多地方，并且有许多不同的变体。当然，没有一个公开的选项是合适的。拯救这一天的是 [CRC RevEng](https://reveng.sourceforge.io/) ，这是一个专门构建的工具，仅从捕获的示例数据中，就可以计算出给定 CRC 是如何工作的。有用！(对于长数据包有一点小问题)

现在，要将代码转换成真正的无线信号，只需要一个 SDR 和 GNU 无线电。这里的技巧是破坏空中的合法信号，然后在中间发送你的假命令。有了这个，你就是记分员了。给你儿子的篮球队额外加 100 分可能很有趣，但这完全会引起别人的注意。[三振出局]有一些狡猾的建议。其中最聪明的是比平时快 10%,以领先优势取胜。或者，在半场结束时改变控球指标，让你的球队在下一次跳球时控球。或者甚至为了一个额外的、不收费的超时而破坏记分牌。因为我们的*完全随机* AES 密钥对于这些单元中的每一个都是相同的，所以你可以在你遇到一个单元的任何地方进行破坏。任何人都可以得到额外的奖励，他们编写了一个 wardriver 程序，寻找记分牌信号。

## 像素补丁令人困惑

谷歌 5 月份的安全公告在引导装载程序中包含了一个看起来很严重的 RCE。引导加载程序作为攻击媒介特别有趣，因为大多数设备会让你刷新旧的、潜在易受攻击的引导加载程序，而不是更新的。谷歌的安全团队非常熟悉这种伎俩，并有一个防范措施，反回滚功能。一个新的引导加载程序将包含一个引导加载程序版本，该版本将永久写入设备，比该版本旧的固件将拒绝写入闪存。

这个 RCE 已经够糟糕了，以至于谷歌把反回滚时间提高到了 11 秒 13 秒。所有这些喧嚣[说服了艾沙德的【加涅罗特·乔治】去看一看](https://eshard.com/posts/pixel6_bootloader)。他带我们踏上了一段精彩的旅程，通过逆向工程修补程序，然后最后提醒我们，这是一个很难做到的事情，因为谷歌开源了他们的引导加载程序。很狡猾。[第 2 部分](https://eshard.com/posts/pixel6bootloader-2)是关于读取和写入原语的更多信息，以及用它们实现面向返回的编程(ROP)漏洞。你不会从帖子中得到复制粘贴的漏洞，但肯定是朝着正确方向的一个很好的推动。

## Kaminski 和隐藏的 DNS 解析器

我们之前讨论过丹·卡明斯基的 DNS 攻击。DNS 使用 UDP，欺骗 DNS 响应太容易了，特别是当您可以控制给定解析器在给定时间请求什么域时。该攻击被私下透露给主要供应商，并在 2008 年修复。我们知道它是固定的，因为我们可以扫描世界上的 DNS 解析器。但是，我们无法检查的解析器怎么办？那些都修好了吗？由于 DNS 解析器只对可信方开放，并且隐藏在公司的防火墙后面，它肯定是安全的。

除了 DNS 现在用于垃圾邮件检测。如果您不得不使用这些技术，我很抱歉—但是发件人策略框架(SPF)；域密钥识别邮件(DKIM)；和基于域的消息验证、报告和一致性(DMARC)都使用 DNS 记录来存储有关电子邮件设置的信息。向 user @Corp.com 发送电子邮件，Corp.com 的电子邮件服务器可能会对您的发送域进行多次 DNS 查找。因此，这些隐藏的解析器不再隐藏。那么结果如何呢？仅仅扫描了 7000 个域名，就发现全球有 25 台服务器仍然容易受到卡明斯基攻击。

## 比特和字节

[Wireshark 4.00 已经发布](https://www.wireshark.org/docs/relnotes/wireshark-4.0.0.html)。有一些新的协议支持，和你所期望的正常的库碰撞。一些功能在速度上有所提升，界面也有所改进。

想要一个硬件安全令牌，但真的希望它完全开放吗？Tillitis 可能适合你。这是一个 USB 平台，用于试验新的安全关键思想，并且是完全开源的，包括硬件。现在还没有地方可以订购，但是你可以让你最喜欢的 PCB 制造商为你制造一个。第一个版本还缺少一些高价值用例真正需要的硬件强化，但这个项目值得关注。

谷歌发布了[黑客谷歌游戏/体验](https://h4ck1ng.google/home)。这是一系列的夺旗挑战，只是为了好玩，但也是解决安全问题的好方法。

基于一个已知的 WebKit 漏洞，又有一个 PS5 漏洞正在开发中。欺骗控制台的浏览器加载一个伪造的文件，你就触发了这个漏洞。它很有用，但仍然是一项正在进行中的工作，还没有击败虚拟机管理程序或运行任意代码。

上周我们报道了一个虚假的求职骗局，本周[是一个虚假的招聘人员](https://www.spiderfoot.net/uncovering-a-fake-recruiter-scam/)。一封电子邮件引起了[ [osint_matter](https://twitter.com/MatterOsint) ]的注意，因为它写得很好，发送到了一个商业地址，并且正确设置了电子邮件 DNS 记录。它链接到一个看起来不错的招聘网站:MHS partners。也许这是合法的？啊，不，那个网站充满了股票照片，合作伙伴的名字是指美国电视节目。用谷歌图片搜索这些照片，出现了其他类似的网站，只是公司名称不同。虽然这是一个运行较好的骗局，但它似乎仍然是一个网络钓鱼探险。在这种情况下，寻找简历和其他信息出售或以其他方式滥用。