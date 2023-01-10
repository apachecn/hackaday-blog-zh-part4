# 本周安全:浏览器中的幽灵，小心你克隆的东西

> 原文：<https://hackaday.com/2021/03/19/this-week-in-security-spectre-in-the-browser-be-careful-what-you-clone-and-hackintosh/>

谷歌一直致力于缓解 Spectre 攻击，并提供了一个可以在浏览器中运行的概念验证。Spectre 是引发一系列推测性执行漏洞和修复的问题之一。谷歌所展示的是，幽灵攻击实际上可以在浏览器中用 Javascript 实现。Spectre 仅限于读取分配给同一进程的内存，现代浏览器已经实现了类似于[站点隔离](https://www.chromium.org/Home/chromium-security/site-isolation)的措施，将每个站点放在一个单独的沙盒进程中。

这些安全特性并不意味着没有来自 Spectre 的实际危险。攻击者可以通过多种方式在另一个站点上运行 Javascript，从简单的交互式广告到跨站点脚本注入。谷歌已经制作了[功能和指南来减轻这些危险](https://security.googleblog.com/2020/07/towards-native-security-defenses-for.html)。

[通过哔哔声计算机](https://www.bleepingcomputer.com/news/security/google-shares-spectre-poc-targeting-browser-javascript-engines/)。

## Git 漏洞翻新

[CVE-2021-21300 是一个问题](https://github.com/git/git/security/advisories/GHSA-8prw-h3cq-mghm)，恶意的 git 存储库可以在克隆过程中执行脚本。限制是克隆必须位于不区分大小写的文件系统上，Git 必须允许符号链接，并且必须启用清理/涂抹过滤器。在 Git for Windows 的情况下，这种组合恰好是默认的。听起来熟悉吗？几个月前，Git for Windows 有一个几乎相同的漏洞，CVE-2020-27955。这可能是第一个漏洞激发了对攻击类型的更多研究，揭示了更多问题的一个实例。在任何情况下，不要从不受信任的存储库中克隆 Git。

## DuckDuckGo 扩展不安全

DuckDuckGo 做一个浏览器扩展，“DuckDuckGo 隐私必备”。这相当简单，阻止一些跟踪方法，并自动重定向到 HTTPS 版本的网站。[Wladimir Palant]对扩展做了一个简短的审计，发现了几个具有讽刺意味的问题。首先，像许多其他反指纹解决方案一样，[扩展本身就是一个指纹](https://palant.info/2020/12/10/how-anti-fingerprinting-extensions-tend-to-make-fingerprinting-easier/)。这些扩展通常依赖于一系列的攻击才能工作，而且无论如何，通常都有可能计算出真实的数据。示例:反指纹扩展可能会设置`screen.width = 1280;`。一个简单的指纹脚本可能只是接受这个值，但是一个更聪明的脚本会接受这个设定值，然后调用`delete screen.width;`并再次检查这个值。反指纹扩展的失败使得用户更容易被识别。注意，这个例子并不是专门来自 DuckDuckGo 扩展，而是[Wladimir]对这些扩展如何出错的解释的一部分。

具体到 DDG 的隐私要素，[有几个更严重的问题](https://palant.info/2021/03/15/duckduckgo-privacy-essentials-vulnerabilities-insecure-communication-and-universal-xss/)。首先，扩展的一个脚本使用`window.postMessage()`在不同的实例之间进行通信。这个函数有点危险，尤其是在扩展中，因为它没有隔离扩展和加载页面之间的消息。如果页面上的脚本确定访问者正在使用易受攻击的 DDG 扩展版本，它可以使用该功能直接发送一些命令。

另一个问题是使用`tabs.executeScript()`的一段代码。该调用使用来自 DuckDuckGo 服务器的数据，没有经过适当的清理。如果恶意代码被托管在扩展从中提取数据的地方，浏览器扩展会很乐意在你访问的每个站点上执行它。[弗拉基米尔]私下向 DDG 通报了他发现的问题，这些问题已经得到解决。他确实指出，不安全扩展的部分责任至少在于扩展 API 本身。在许多情况下，编写安全的扩展代码要比想象中困难得多。

## 面向研究人员的黑客工具

为苹果生态系统做研究或应用开发是一件痛苦的事情。如果你和我一样，那么你就没有兴趣把运行 Mac 作为你的日常驱动。仅用于研发的 Mac 成本也有点高。许多人的标准解决方案是 Hackintosh——在通用硬件或虚拟机上安装 MacOS。我们的老朋友[Sick Codes]有一个让苹果系统变得更加平易近人的项目: [Docker-OSX](https://github.com/sickcodes/Docker-OSX/) 。需要一个 MacOS 系统来运行 Xcode？部署 docker 映像并启动 Xcode，它就托管在您的 Linux 或 Windows 机器上。想对一个苹果二进制做安全性研究？对，就在那里运行，然后开始工作。

现在，有人可能想知道这些解决方案:它们合法吗？苹果的服务条款不是说得很清楚吗，我们无权在任何非苹果生产的硬件上运行 MacOS。嗯，[【病码】也看了一下那个问题](https://sick.codes/is-hackintosh-osx-kvm-or-docker-osx-legal/)。据我所知，他不是律师，所以不要全信。只要你做的是真诚的安全研究，Apple Security Bounty 的条款就会超越正常的服务条款。

## 各种事情

曾经想进入 Linux 内核黑客和开发，但不知道从哪里开始？[乔迪·佐梅尔]刚刚发表了关于这个主题的系列文章的第一部分。这是对编写内核驱动程序的快速介绍，指出了驱动程序中的安全缺陷，然后是利用该缺陷的逐步指南。这看起来是一个需要注意的地方，特别是如果有更多的分期付款。

您的 Netgear 智能交换机可能非常容易被黑客攻击。Ncc 集团从 Prosafe Plus 交换机发布了[他们的一组漏洞。最糟糕的似乎是未经身份验证的用户可以访问调试接口。您可能没有报告中的任何一个确切的开关，但可以肯定的是，这些漏洞中的一些也存在于其他设备中，只是略有不同。](https://research.nccgroup.com/2021/03/08/technical-advisory-multiple-vulnerabilities-in-netgear-prosafe-plus-jgs516pe-gs116ev2-switches/)

有没有想过当你点击谷歌搜索中明显虚假的赞助搜索结果时会发生什么？SUID 的人想知道答案，他们写了一份非常详细的结果报告。简而言之，如果你不幸让恶意广告安装了它们的有效载荷，它们会试图窃取你机器上保存的凭证和其他私人数据。

最后，Nettitude Labs 正在演练攻击者可能使用的技术，以确定目标是否是虚拟机，以及它是什么平台。第一部分是关于虚拟硬件的内存布局，第二部分[讨论每个虚拟机平台的驱动行为](https://labs.nettitude.com/blog/vm-detection-tricks-part-2-driver-thread-fingerprinting/)。我们有时会使用虚拟机运行危险的二进制文件和访问可疑的网站，因此熟悉一些检测和逃脱策略是很有用的。