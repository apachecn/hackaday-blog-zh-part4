# 本周安全:打破 CACs 修复 NTLM，有史以来最大的漏洞，并通过打破它修复火狐

> 原文：<https://hackaday.com/2022/07/08/this-week-in-securitybreaking-cacs-to-fix-ntlm-the-biggest-leak-ever-and-fixing-firefox-by-breaking-it/>

首先，微软 6 月份的安全补丁修复了针对 NTLM 的中间人攻击 [CVE-2022-26925](https://msrc.microsoft.com/update-guide/en-US/vulnerability/CVE-2022-26925) 。根据 NIST 的说法，[这种攻击正在被广泛利用](https://www.cisa.gov/uscert/ncas/current-activity/2022/07/01/cisa-adds-one-known-exploited-vulnerability-catalog)，所以它出现在 KEV(已知被利用的漏洞)目录中。该列表跟踪需要解决的最重要的漏洞，并在 7 月 22 日之前触发强制补丁安装。奇怪的是，微软修复 CVE-2022-26925 的补丁还包括对 CVE-2022-2693、[certified](https://hackaday.com/2022/05/13/this-week-in-security-f5-twitter-poc-certifried-and-cloudflare-pages-pwned/#certifried)等几个证书漏洞的修复。该漏洞是一个机器证书可以被重命名为与域控制器相同的名称，从而导致整个组织的危害。

6 月份推出的[补丁现在需要一个“强证书映射”来将用户与证书绑定在一起。拥有相同的公用名已经不够了，像安全标识符(SID)这样的安全值必须在 Active Directory 中从证书映射到用户。该补丁将 AD 置于兼容模式，只要用户帐户早于安全证书，该模式就接受不安全的映射。这产生了一个意想不到的后果](https://support.microsoft.com/en-us/topic/kb5014754-certificate-based-authentication-changes-on-windows-domain-controllers-ad2c23b0-15d8-4340-a468-4d4f3b188f16)[破坏了美国政府使用 CACs(通用访问卡)](https://www.cisa.gov/guidance-applying-june-microsoft-patch)来验证用户身份的方式。政府机构通常通过发布 CAC 开始他们的入职，然后为该用户建立一个 AD 帐户。这会使证书变旧，这意味着最新的补丁会拒绝它。值得庆幸的是，有一个可以设置的注册表项，允许旧的映射仍然工作，尽管结果可能会有一点安全漏洞。

## 解密器因抄袭而发布？

我们从勒索病毒瘟疫中看到的一个奇怪的事情是，当犯罪集团关闭商店时，解密器被释放。在这种情况下，AstraLocker 已经[关闭了它的门](https://www.bleepingcomputer.com/news/security/astralocker-ransomware-shuts-down-and-releases-decryptors/)，并发布了一组解密例程。虽然那些解密程序已经被证明是有效的，但如果你碰巧是其中一个不幸的受害者，那就等着看像 [Emsisoft 这样的知名组织把那些可疑的工具打包成一个已知良好的解决方案](https://www.emsisoft.com/ransomware-decryption-tools/free-download)。

为什么一个团体会关闭并释放他们王国的钥匙？在某些情况下，这是因为执法机构越来越近，令人不安，夹具只是了。在这里，似乎有一个模仿团体已经开始在 Astralocker 上发布他们自己的版本。AstraLocker 2.0 的问题在于它是一个“砸了就抢”的游戏，一个似乎永远不会提供解密密钥的低强度游戏。一种可能的解释是，这种模仿活动正在破坏原演员的“好名声”，并使说服受害者为解密付费变得更加困难，从而导致了退休。

## 中国警方泄露数据库

我们过去报道过一些数据库漏洞，整个国家都暴露在外，但这次似乎是小菜一碟。超过 10 亿用户在中国警方数据库泄露事件中暴露，这可能是一篇博客帖子中无意泄露的凭据造成的。该数据库以 10 个比特币的价格出售，比一个比萨饼的价格还低。那个帖子已经从提供它的论坛上被删除了。这可能是有史以来最大的数据库泄漏，在这种规模下，很难再有更高的了。

## 火狐杀毒软件

Mozilla 正在 Firefox 中开发一个新的 JavaScript 特性， [Sanitizer](https://developer.mozilla.org/en-US/docs/Web/API/HTML_Sanitizer_API) 。这是通过添加一种标准化的方法来净化数据，从而挫败跨站点脚本(XSS)攻击的一种努力。部分原因是，当谈到 HTML 将如何被理解时，浏览器本身可以是一个非常可靠的“真理”来源。

这是一个仍在建设中的实验性功能，但它可供测试，研究人员已经开始努力使它变得更好。[Gareth Heyes]尝试了一下，[发现了 SVG 处理的一个潜在问题](https://portswigger.net/research/bypassing-firefoxs-html-sanitizer-api)。SVG 是由 XML 代码生成的图像，有效元素之一是一个`use`语句，本质上包括来自其他地方的 SVG 代码。其他地方可能存在潜在的恶意，一些非常巧妙的工作可能导致任意 JavaScript 执行。Firefox 102 修复了这个缺陷，理想情况下，当这个功能到期时，所有这些缺陷都将被解决。如果它被证明是有用的，Chrome 将会采用它，它甚至可能会成为一个网络标准。

## 比特和字节

Project Zero 对他们今年到目前为止跟踪的野生昆虫进行了概述。总共有 18 个 bug，但其中 9 个是以前 bug 的变体，即修复已知问题的补丁不足以真正修复根本问题的情况。在一些情况下，它甚至不是一个变种，而是被修复的完全相同的错误，然后再次变得易受攻击。如果没有别的，这是回归测试价值的有力证明。

英国军队的官方 Twitter 和 YouTube 账户[本周被恶意第三方访问](https://cointelegraph.com/news/british-army-s-social-media-accounts-hacked-by-crypto-scammers)。通过这种访问，所有发布的都是加密诈骗网站的链接——很难实现访问如此有价值的帐户的潜力。显然不是政府资助的演员。

最后，在安全软件引入安全漏洞的悠久传统中，趋势科技修补了一个漏洞，该漏洞允许通过 Windows 上的挂载点操作来提升权限。该问题已被发现并私下报告，修复已在 17.7 版本中推出。没有迹象表明这个曾经被利用过，所以为好人写一个吧！