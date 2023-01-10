# 本周安全:Chrome 语音错误、UDP 碎片和 Citrix 大漏洞

> 原文：<https://hackaday.com/2020/01/24/this-week-in-security-chrome-speech-bug-udp-fragmentation-and-the-big-citrix-vulnerability/>

Chrome 浏览器最近修复了一个严重的安全漏洞，CVE-2020-6378。CVE 的报告仍然标记为私人的，就像[的错误报告](https://bugs.chromium.org/p/chromium/issues/detail?id=1018677)一样。我们有的只是“在语音识别器中释放后使用”。我们是否运气不佳，试图了解更多关于这个漏洞的信息？如果你仔细查看私有的 bug 报告，你会注意到它在 Chromium bug tracker 中。Chrome 主要基于 Chromium 项目，添加了一些专有特性。由于 Chromium 是开源的，我们可以找到修复这个 bug 的代码更改，并可能了解更多。

关闭到铬源，[镜像到 Github](https://github.com/chromium/chromium) 。我们可以查看每一次提交，并最终找到我们要找的那一次，但是 Chromium 提交消息通常包含一个由该提交修复的 bug 的引用。所以，我们可以使用 Github 的搜索功能来查找提到 1018677 的提交。就这样，我们找到了[单次提交](https://github.com/chromium/chromium/commit/57f988dd7c1f63f59b44282efcc9e6f1e85ac19c)和更多信息。

提交消息中提到的关闭可能是指浏览器被关闭，但也可能是指标签进行语音识别，甚至是语音系统本身。因为多个部分被并行卸载，所以在调用中止对象和从内存中卸载该对象之间存在竞争条件。这种竞争可能导致典型的释放后使用，将代码执行转移到已经释放的内存位置。

所有这些都很有趣，但这如何保证一个关键的评级呢？进入[网络语音 API](https://developers.google.com/web/updates/2013/01/Voice-Driven-Web-Apps-Introduction-to-the-Web-Speech-API) 。我只是猜测一点，但是很可能这个 API 使用了有问题的语音识别器代码。它甚至可能与触发崩溃的安全提示交互。假设一个攻击页面试图使用语音 API，然后在用户可以响应提示之前释放 API 对象。这可能是已经发现的情况，尽管我们现在还在猜测。

### 远程桌面网关

微软的远程桌面网关产品中的一对预认证漏洞最近得到了修复。[这些漏洞都围绕着 UDP 支持](https://www.kryptoslogic.com/blog/2020/01/rdp-to-rce-when-fragmentation-goes-wrong/)、碎片以及传入数据包的哪些元素可以信任。

第一个漏洞是最严重的:UDP 片段重组代码部分信任数据包中声明的片段数量。基于该数字分配缓冲区。将传入数据包复制到缓冲区的代码首先检查复制的字节数不会超过分配的字节数。看起来这应该是一个足够的检查，但这忽略了数据包被写入的偏移量。单个包可以声称只有两个包，但将其自己的碎片数设置为任意值。写偏移量基于这个值，因为写入的字节总数没有超过缓冲区长度，所以代码很乐意将传入的数据写入任意位置。

Robert Graham 在 twitter 上提出了[这个有趣的观点，即尽管这里的代码使用了一个被认为是安全的内存复制例程`memcpy_s`，但这个漏洞仍然存在。这个安全的例程*确实*阻止代码超过缓冲区的结尾，但是在这种情况下，整个操作都在数组之外，这是官方未定义的行为。任何时候看到“未定义的行为”，只要在心理上用“真的很危险，以后注定要烧死你”来代替就好了。](https://twitter.com/ErrataRob/status/1219019660756242432)

第二个 vuln 假设片段的数量永远不会超过 64。分配 64 个整数的数组来跟踪接收到了哪些片段。当处理传入的片段时，只要片段数小于指定的片段数，就会向该数组中的相应位置写入 1，即使它已经超过了所分配内存的末尾。

### Internet Explorer 0 天

IE 9、10 和 11 [中的传统`jscript.dll`脚本引擎有一个漏洞，该漏洞正在被恶意利用](https://threatpost.com/microsoft-zero-day-actively-exploited-patch/152018/)，与内存中对象的处理有关。Jscript 是微软对 Javascript 的重新实现，为了兼容，页面可以请求其代码在旧引擎中运行。

微软正在等待下一个补丁星期二推出修复，但已经建议了一个变通办法。设置`jscript.dll`文件权限，使其不可读。有一些缺点，如中断 Windows Media Player 中的 MP4 播放，阻止 SFC 扫描完成，以及其他一些问题。

我们都在等着看微软是否会选择在下个月对 Windows 7 进行修复。如果没有，请将此记为仍在运行 Windows 7 的机器的第一个突出问题。

### Citrix 和横向路径

首先，[一些 Citrix 产品包含 CVE-2019-19781](https://threatpost.com/citrix-patch-rollout-critical-rce-flaw/152041/) ，这是一个路径横向缺陷。这种类型的缺陷通常涉及攻击者请求包含“..”的路径绕过安全控制。在这种情况下，攻击者可以在认证之前滥用这个漏洞，让[下载凭证](https://github.com/projectzeroindia/CVE-2019-19781)，甚至让[获得一个远程外壳](https://github.com/trustedsec/cve-2019-19781/)。

它正被积极利用，因此 Citrix 将他们的补丁发布日期提前到了今天(1 月 24 日，星期五)。到目前为止，还不清楚有多少设备已经受到威胁，但这个漏洞是非常严重的。

### Connectwise 和勒索软件

Connectwise 是一个远程桌面和管理解决方案。很明显，去年袭击 22 个独立城市的德州勒索软件攻击中使用的攻击载体是[。这些漏洞很简单，比如跨站请求伪造、跨站脚本等等。](https://know.bishopfox.com/advisories/connectwise-control)

这个故事最有趣的部分可能是 Connectwise 的回应。在一次会议上，他们的一名高管威胁要提起诽谤诉讼。第三方已经[验证了这些漏洞，因此研究人员很可能是正确的，这很可能是勒索软件攻击的原因。](https://blog.huntresslabs.com/validating-the-bishop-fox-findings-in-connectwise-control-9155eec36a34)

### 谷歌黑客组织——GGvulnz

最后一个故事模糊了漏洞和简单社会工程之间的界限。【米兰·马扎尔】注意到很多公司使用谷歌群，但是[没有正确设置权限](https://medium.com/@milanmagyar/ggvulnz-how-i-hacked-hundreds-of-companies-through-google-groups-b69c658c8924)。简单地公开内部讨论本身就有问题，但是这里有更聪明的方法。你看，许多谷歌团队使用公司域名的专用电子邮件地址。这通常不被认为是一个问题，但是一个攻击会对一个公司域名上的电子邮件地址做什么呢？

有些服务，比如 Slack，可以配置成自动批准新账户，只要它们来自公司的电子邮件地址。这种想法通常会限制员工的访问权限。如果有一种简单的方法可以访问公司的电子邮件地址会怎么样？

是的，这就是攻击。使用 mailinglist@companyname.com 作为注册邮箱，建立一个备用账户。然后，从谷歌群页面上抓取确认链接，享受你的官方 Slack 账户。

米兰已经从谷歌、Slack 等公司得到了回应。虽然这是一种非常巧妙的攻击，但它并不完全是他们系统中的漏洞，而是客户的错误配置。在某些方面，这类问题是我最感兴趣的。从技术上来说，没有什么是坏的，但是这些策略的重叠导致了一个非常聪明的攻击。

如果你知道一些聪明的、有趣的或者有安全新闻价值的东西，一定要让我们知道，我们将在下周报道它！