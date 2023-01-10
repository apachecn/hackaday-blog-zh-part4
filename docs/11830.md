# 本周安全:对抗勒索软件、Unicode、话语和无根

> 原文：<https://hackaday.com/2021/11/05/this-week-in-security-the-battle-against-ransomware-unicode-discourse-and-shrootless/>

我们经常谈论勒索软件团伙，但在这个舞台上还有另一个模糊、松散的参与者群体。 [Emsisoft 揭示了一个由研究人员和执法机构组成的网络，他们在幕后努力挫败勒索病毒活动。](https://blog.emsisoft.com/en/39181/on-the-matter-of-blackmatter/)

黑暗面是一个有趣的案例研究。这是一个因袭击殖民管道而成为全球头条新闻的组织，它关闭了管道六天。你可能没有意识到的是，从 2020 年 12 月中旬到 2021 年 1 月 12 日，黑暗面勒索软件的加密算法有一个弱点。有趣的是，Bitdefender 在 1 月 11 日发布了一个解密器。我还没有找到证实，但时间似乎表明，解密器的发布引发了黑暗面寻找和修复他们的加密漏洞。(或者，它可能是作为对修复的回应而发布的，时区扭曲了日期。)

Emsisoft 非常小心，当他们发现勒索软件中的漏洞时，不会泄露他们的秘密。相反，他们有一个执法和安全专业人员的网络，他们分享信息。当黑暗面组织以 BlackMatter 的名字重新成立时，这又派上了用场。

在活动再次开始后不久，加密代码中再次出现了一个类似的漏洞。勒索软件的隐藏网站，用于协商解密付款，似乎有一个漏洞，Emsisoft 可以用来跟踪受害者。由于他们有一个工作的解密器，他们能够直接接触，并为受害者提供解密工具。

当 BlackMatter 门户网站的链接在 Twitter 上泄露时，这种情况发生了变化。看起来很多人对勒索软件团伙不太重视，并利用这个机会通过传送门告知了 BlackMatter 这个事实。作为回应，BlackMatter 关闭了该门户网站，切断了 Emsisoft 的信息渠道。此后，加密漏洞被修复，Emisoft 无法再监听 BlackMatter，他们发布了这个故事，鼓励 BlackMatter 受害者联系他们。他们还建议勒索软件受害者总是联系执法部门来报告事件，因为可能有一个尚未公开的解密器。

最后，最新消息是 [BlackMatter 正在关闭](https://www.bleepingcomputer.com/news/security/blackmatter-ransomware-claims-to-be-shutting-down-due-to-police-pressure/)。通知将执法行动作为关闭的部分原因，并提到了“最新消息”。据推测，这是指[10 月 26 日在乌克兰和瑞士的逮捕](https://www.bleepingcomputer.com/news/security/police-arrest-hackers-behind-over-1-800-ransomware-attacks/)。

## AtomSilo 和 LockFile

Avast 发布了一个解密器,涵盖了 AtomSilo 和 LockFile 勒索软件程序。这是基于[jiří·文帕尔]的工作。这是一个简单的工具，可以备份加密文件，然后尝试解密它们。赢家。

## 要 FTP，还是不要 FTP？

谷歌已经策划从 Chrome 中移除 FTP 协议很长时间了，随着版本 95 的推出，[他们终于完成了任务](https://www.chromestatus.com/feature/6246151319715840)。不再有重新启用 FTP 的标志，代码已经从项目中清除。值得一提的是，Firefox 也禁用了 FTP 支持。这种改变的原因是为了消除攻击面，并消除对很少使用的特性的代码维护。谷歌指出，有非常好的专用 FTP 客户端，我们应该使用。

## 隐藏在 Unicode 中

[尼古拉斯·鲍彻]和[罗斯·安德森]提交了一篇论文，详细描述了一个真正独特的 Unicode 攻击。这不是我们第一次研究 Unicode 如何导致安全问题，也不会是最后一次。这里的问题是将文本标记为从左到右和从右到左的 Unicode 字符。由这些字符创建的块可以嵌套，导致一些意想不到的结果。让我们来看看:

```

bool isAdmin = false;
/* begin admins only */ if (isAdmin) {
    printf("You are an admin.\n");
/* end admins only */ }

```

神奇之处在于评论。下面是编译器看到的，但是 Unicode 扩展成了助记符:

```

/*RLO } LRIif (isAdmin)PDI LRI begin admins only */
    printf("You are an admin.\n");
/* end admins only RLO } LRI*/

```

由于编辑人员会尊重 Unicode 控制字符，手工代码审查将会错过这些诡计。因为字符在注释中，编译器会忽略它们，并按照实际编写的那样编译程序。真正的危险是当这种技术与其他供应链攻击技术结合在一起时。

对于一个新的编码者来说，典型的第一个补丁是清理空白和注释。这就引入了这样的补丁有恶意的可能，不用十六进制编辑器看是看不出来的。作者提出了三个缓解建议:编译器警告、禁止这种 schenanigans 的正式语言规则，以及在文本编辑器和相关工具中可见的 Unicode 字符。

锈语[已经在这个问题上采取了行动](https://blog.rust-lang.org/2021/11/01/cve-2021-42574.html)。最新版本 1.56.1 包含一个编译器 lint，它拒绝可能有问题的 Unicode 字符。Github 还在检测到这些字符时[推出了警告](https://github.blog/changelog/2021-10-31-warning-about-bidirectional-unicode-text/)。虽然新的关注是受欢迎的，但请注意[这是一个已知的问题已经有一段时间了](https://skylightcyber.com/2019/05/12/ethereum-smart-contracts-exploitation-using-right-to-left-override-character/)。

## 恶搞亚马逊到 RCE 的话语

【joernchen】[发布了一个关于 web 应用](https://0day.click/recipe/discourse-sns-rce/)的缺陷。Discourse 有一个公开的端点`/webhooks/aws`，它导致对`open()`的调用，已知使用不可信的数据进行调用是危险的。这里的保护措施是，所提供的数据必须由 Amazon 提供的签名证书进行签名，因为这个端点专门用于 AWS 的简单通知服务。乍一看，似乎防弹。

问题是用于验证的 PEM 证书是由传入数据指定的。正则表达式验证该证书的 url 确实在 Amazon 上。Ruby 的 OpenSSL 证书解析函数愿意忽略额外的 XML，只要它在给定的数据中找到嵌入的有效证书。

因此，攻击者需要做的就是在 Amazon AWS 设置中的正确位置托管一个 PEM 证书，并指定一个将嵌入该证书的 URL。Discourse 检查`.pem` URL，验证它与正则表达式匹配，并愉快地确认请求与证书匹配，从而运行攻击者提供的代码。该缺陷已在 2.7.9 和最新的 2.8.0 测试版中得到修复。如果你在运行 Discourse，去确保你有这个更新。

## 微软攻破 macOS

令人幸灾乐祸的是，微软宣布了他们在 macOS 中发现的一个漏洞。这可能会让攻击者绕过苹果公司名不副实的系统完整性保护(SIP)。在这种情况下，SIP 不是 VoIP 协议，而是一种防止根用户对系统进行某些修改的技术。SIP 在某些地方也被称为无根。以前也发现过无根旁路。例如，如果一个内核驱动程序有一个漏洞，在内核环境中运行代码会自动破坏这种保护。

新的旁路非常简单。当安装 Apple 签名包时，它们是在超级根上下文中完成的。一些软件包运行一个安装后脚本，该脚本使用`zsh` shell 运行。当`zsh`被调用时，它自动运行`/etc/zshenv`脚本。问题已经很明显了吗？把你的越狱代码推送到`zshenv`，安装一个包，系统自动运行。打得好。