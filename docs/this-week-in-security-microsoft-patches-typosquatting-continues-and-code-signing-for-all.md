# 本周安全:微软补丁，域名仿冒继续，所有代码签名

> 原文：<https://hackaday.com/2022/11/11/this-week-in-security-microsoft-patches-typosquatting-continues-and-code-signing-for-all/>

我们一直在跟踪的两个 Outlook 漏洞终于在本周二得到了修复，总共有六个漏洞是 0 天漏洞。第三个漏洞也是 0-day，由 Google 威胁分析小组发现。当 Windows 客户端连接到恶意服务器时，这将导致任意代码执行。

修复了一对特权升级缺陷，一个是另一个打印假脱机问题，另一个是密钥处理服务的一部分。最后的零日修复是绕过 web 标记，这是添加到文件元数据中的标签，表明它是从互联网上下载的。如果您将恶意软件放在 ISO 中或在 zip 文件中标记为只读，它在执行时不会显示警告。

## 比特币会出现错别字吗

一个没有放缓迹象的趋势是域名仿冒，这是一种简单的恶意软件分发策略，使用合法软件包名称的拼写错误来上传受感染的软件包。由 Phylum 的研究人员发现的最新方案[，在 Python 包中提供了一个密码窃取器。这些包被托管在 PyPi 上，命名为`baeutifulsoup4`和`cryptograpyh`。这些软件包安装了一个在浏览器后台运行的 JavaScript 文件，并监控剪贴板上的加密货币地址。检测到时，目标地址将被替换为攻击者控制的地址。](https://blog.phylum.io/pypi-malware-replaces-crypto-addresses-in-developers-clipboard)

## 旧缺陷

说到剪贴板，[谷歌的 Project Zero 让我们了解了一个来自 2020 年的故事](https://googleprojectzero.blogspot.com/2022/11/a-very-powerful-clipboard-samsung-in-the-wild-exploit-chain.html)，三星设备被一个从剪贴板开始的利用链利用。三星建立了一个定制的剪贴板服务，支持剪贴板上的图像文件。一个疏忽允许设备上的任何应用程序请求任何文件的句柄。这是用来丢弃第二阶段二进制文件的。第二个应用程序，三星的文本到语音系统，通过覆盖一个设置文件被劫持，导致恶意二进制文件而不是有效的语音引擎被启动。这一步提升特权，因为语音引擎作为一个`system_app` SELinux 上下文启动。

第二个漏洞是信息泄漏，内核日志被复制到一个可由`system_app`上下文读取的文件中。在 GPU 驱动程序中触发警告导致地址信息被记录到该文件中。泄露几次，你就破解了内核地址空间布局随机化，更不用说第三个漏洞中使用的指针值了。

最后一个是 DECON 驱动程序、显示和增强控制器(图形堆栈的一部分)中的“释放后使用”。打开一个文件描述符并与用户空间共享。用户空间可以释放描述符，驱动程序继续将其视为有效。在释放和访问之间，文件描述符的许多恶意副本被喷入内存，希望一个这样的副本将占用释放的地址。这个伪描述符允许恶意软件跳转到内核空间，并提升其用户空间组件作为`vold`上下文运行，也称为卷守护进程。达到这一水平的恶意软件是 Android 城堡之王。

这个漏洞链是在野外发现的，并于 2021 年 3 月修复，但它仍然是一个关于漏洞利用是如何完成的漂亮外观。在这种情况下，它被认为是来自商业供应商-NSO 集团或类似的机构。

## 代码签名

让我们加密是伟大的。您控制一个域，您可以生成一个免费的 SSL 证书，用于加密和验证该域的 HTTPS 流量。你可能在某个时候问过自己，你能使用 Let's Encrypt 来签署二进制文件吗？这将是有用的，但遗憾的是这不是一个选项。因此，本周非常受欢迎的消息是 Sigstore 现在已经普遍可用，并且 [Trail Of Bits 有故事](https://blog.trailofbits.com/2022/11/08/sigstore-code-signing-verification-software-supply-chain/)。

这里的关键是，您可以让您的代码由一个短期证书签名，该证书证明了一个 OpenID 身份。有用的 OpenID 服务的例子有 Github、Google 和 Microsoft accounts。所以你可以得到一个签名，绑定到你的公共身份，完全不用担心证书管理。关注 Sigstore，因为它看起来有一个光明的未来，作为代码签名的 Let's Encrypt。

## 像素锁定旁路

在 Android 的锁屏中有一个简单而关键的错误，[被【David schütz】](https://bugs.xdavidhu.me/google/2022/11/10/accidental-70k-google-pixel-lock-screen-bypass/)在 6 月份发现，奇怪的是被谷歌搁置了几个月，最终在 11 月的安全更新中得到修复。由于忘记了 SIM 卡密码，这个发现纯属偶然。你知道你的 SIM 卡有一个 PIN 码可以用来锁卡吗？如果你忘记了，SIM 卡的文档里有一个 PUK，一个个人解锁密钥。

用 PIN 保护的 SIM 卡启动你的手机，三次解锁失败，手机进入锁定模式，需要 PUK 解锁。这个过程由 Android 安全屏幕处理，通过 PUK 成功解锁 SIM 卡触发了一个`.dismiss()`函数调用。问题是多个安全屏幕可以同时被激活，包括你的锁屏，而`.dismiss()`调用被栈顶处理。SIM 卡被解锁，这改变了屏幕的堆叠，解锁屏幕通常位于堆叠的顶部，弹出手机。

现在请注意，这种利用不解密手机。它在冷启动时不起作用。但是一部已经认证过一次的开机手机，仅仅是被锁定，就可以用这种方式解锁。很可能是谷歌的工程师无法重现这个问题，所以它没有得到应有的快速处理。在亲自演示了这个问题之后，变革的车轮开始转动，补丁终于发布了,[David]获得了非常丰厚的 70，000 美元奖金。这也是 AOSP 的一个问题，因此 LineageOS 等下游项目正在推出补丁，并致力于发布补丁。

## 比特和字节

25 种不同的联想笔记本电脑无意中附带了开发驱动程序，允许从操作系统内部操纵 NVRAM 变量。或者更简单地说，[你可以在 Windows](https://arstechnica.com/information-technology/2022/11/lenovo-patches-secure-boot-vulnerabilities-that-imperil-25-notebook-models/) 中关闭安全引导。受影响型号的更新修复了固件，以禁止在引导后对此类设置进行操作。

Google Play 商店上的一系列恶意应用程序已经获得了 100 万次下载。这些应用程序在安装后会将任何恶意活动延迟几天，但最终会在新的 Chrome 标签中加载钓鱼网站。真正令人担忧的是，这些应用程序进入了 Play Store，并且没有在谷歌的任何应用程序扫描中被标记出来。这让人不禁想知道还隐藏着什么。

还有一些积极的消息，Open Bug Bounty 已经过了[修复百万漏洞](https://appdevelopermagazine.com/open-bug-bounty-has-fixed-1-million-vulnerabilities/)的里程碑。这种替代的 bug bounty 系统是为较小的站点和组织设计的，以吸引安全人才来发现其基础结构的问题。它似乎正在工作，祝贺里程碑！