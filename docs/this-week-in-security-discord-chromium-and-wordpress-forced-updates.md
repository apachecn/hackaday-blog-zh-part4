# 本周安全:不和谐，铬，和 WordPress 强制更新

> 原文：<https://hackaday.com/2020/10/30/this-week-in-security-discord-chromium-and-wordpress-forced-updates/>

[Masato Kinugawa]发现了一系列错误，当这些错误串在一起时，[允许在 Discord 桌面应用](https://mksben.l0.cm/2020/10/discord-desktop-rce.html)中远程执行代码。Discord 的桌面应用程序是一个电子驱动的应用程序，这意味着它是一个在捆绑的轻量级浏览器上呈现的网页。在 JavaScript 上构建桌面应用程序当然让开发者的生活更轻松，但这也意味着你继承了运行浏览器和 JS 的所有问题。里面有一个关于最终实现全栈 JavaScript 的笑话。

electronic 最大的安全问题是一个简单的跨站脚本(XSS)错误突然在桌面环境中运行，而不是在浏览器中。是的，有一个沙盒选项，但必须手动启用。

这就引出了第一个问题。`sandbox`和`contextIsolation`选项都没有设置，所以都默认为 false。这种设置允许攻击者做什么？因为前端和后端 JavaScript 在相同的上下文中运行，所以 XSS 攻击有可能覆盖 JS 函数。如果后端调用这些函数，它们就可以完全访问 Node.js 函数，包括 exec()，这时转义就完成了。

现在我们知道了如何逃离电子公司的网络浏览器，我们能用什么来进行 XSS 攻击呢？答案是自动内嵌 iframe。例如，只要看看下面的漏洞利用演示。在后端，我所要做的就是粘贴 YouTube 链接，WordPress 编辑器施展魔法，自动将视频嵌入 iframe。Discord 对一些不同的服务做同样的事情，其中一个是 Sketchfab。

这让我们想到了第二个弱点。Sketchfab 嵌入有一个 XSS 漏洞。一个特制的 sketchfab 文件可以在用户与嵌入式播放器交互时运行一些 JS，这可能会导致不和谐。我们就要到了，但是还有一个问题。这段代码运行在 iframe 的上下文中，而不是主线程中，所以我们仍然不能覆盖函数来实现完全转义。要真正获得完整的 RCE，我们需要触发导航到主页面视图中的恶意 URL，而不仅仅是 iframe。已经有代码防止 iframe 重定向首页，所以这个 RCE 是个失败，对吗？

输入 bug #3。如果首页和 iframe 在不同的域中，阻止导航的代码永远不会触发。在这种情况下，iframe 中运行的 JavaScript 可以将首页重定向到恶意网站，然后该网站可以覆盖核心 JS 函数，导致完全逃到 RCE。

这是一个非常聪明的漏洞链，从 Discord 应用程序到 Sketchfab 中的 XSS，再到 Electron 本身的一个 bug。虽然这个特殊的例子需要与嵌入的 iframe 交互，但是很有可能另一个易受攻击的服务有一个不需要交互的 XSS 错误。在任何情况下，如果你在桌面上使用 Discord，请确保应用程序是最新的。然后，欣赏下面嵌入的攻击演示。

 [https://www.youtube.com/embed/0f3RrvC-zGI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/0f3RrvC-zGI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



### 铬游离型溢流

Chromium 86 对一个特别严重的错误进行了修复。追踪为 CVE-2020-15999，这是一个如何渲染 FreeType 字体的错误。现在微软已经转向 Edgium (Chromium powered Edge)，[我们在 Chromium 漏洞上得到买一送一的待遇](https://portal.msrc.microsoft.com/en-us/security-guidance/advisory/ADV200002)。这个 bug 很有趣，因为据报道它已经被积极利用了。谷歌已经[将这个 bug 公开](https://bugs.chromium.org/p/chromium/issues/detail?id=1139963)，所以我们可以仔细看看到底发生了什么。

问题出在 FreeType 库中，即当字体包含嵌入的 png 时如何处理它们。简单地说，PNG 的宽度和高度以 32 位值的形式存储在字体中，但是在分配缓冲区之前，这些值被截断为 16 位。在这之后，PNG 被复制到缓冲区，但是使用未截断的值。然后执行检查以确保拷贝没有溢出，但是无用的是，[这是在拷贝发生之后检查的。这个 bug 包含了一个测试用例，所以你可以自由地使用这个代码来检查你的设备。目前还不清楚这个 bug 存在多久了，但有可能它也影响了 Android 的系统 WebView，后者更新速度要慢得多。](https://chromium.googlesource.com/chromium/src/third_party/freetype2.git/+/b977dff8c99b19d92f10f20c02acfe8101ce4d6f%5E%21/#F0)

### Chrome 漏洞利用的一步一步

[满月墨]最近发表了一份关于他在三月份发现的免费后使用 Chrome 漏洞的详细报告，追踪号为 CVE-2020-6449。让这篇文章值得一看的是他向我们详细描述了从这个 bug 开发一个有效利用的过程。整个帐户是一个滥用 JavaScript 操纵底层引擎状态的大师级。作为奖励，他还给我们一个链接，链接到[PoC 漏洞代码](https://github.com/github/securitylab/tree/main/SecurityExploits/Chrome/blink/CVE-2020-6449)供我们查看。

### FBI 警告

美国联邦调查局与 CISA 和 HHS 一起向[发出警告](https://us-cert.cisa.gov/sites/default/files/publications/AA20-302A_Ransomware%20_Activity_Targeting_the_Healthcare_and_Public_Health_Sector.pdf)，针对美国医院和其他医疗服务提供商的勒索软件攻击正在不断增加。这次攻击使用了`Trickbot`恶意软件和`Ryuk`勒索软件。他们还注意到使用 DNS 隧道进行数据渗透，并特别提到销售点系统作为目标。

缓解措施在试图解读这里的言外之意时特别有趣。在我们深入研究之前，我必须提出一条过时的建议:“定期更换密码”。这一直是许多用户和管理员的祸根，并导致安全性减弱，而不是增强。说完这些，让我们看看其他的建议。

一些建议是锅炉板，如双因素认证，安装安全更新，有备份等。我很惊讶地看到允许地方管理的建议，以便让事情重新运转起来。最有趣的可能是建议仔细查看正在运行的任何 RDP 服务。这是否意味着某些医疗保健 PoS 系统正在运行过时的 Windows，默认情况下有一个易受攻击的 RDP 服务对网络开放，它突然成为了攻击目标？也许吧。我已经学会了不要太相信这些建议，除非给出实际的细节，而这个特殊的例子在细节上是相当轻的。

### Loginizer 的 SQL 注入

流行的 Loginizer WordPress 插件旨在保护你网站的登录页面免受攻击。它可以添加双因素身份验证、用于重复登录尝试的验证码，甚至可以检测暴力尝试并将违规 IP 列入黑名单。最后一个是问题所在。传入的登录尝试被记录到一个 SQL 数据库中，该记录没有得到适当的清理，也没有使用准备好的语句。因此，登录页面受到了非常简单的 SQL 注入攻击。教训？净化您的输入，并使用准备好的语句！[最新更新](https://loginizer.com/blog/loginizer-1-6-4-security-fix/)修复了这个问题，以及一个单独但类似的安全问题。

这个 bug 的新颖之处在于，WordPress 发现这是一个足够大的问题，打破玻璃，按下标有“强制更新”的红色大按钮。我不知道 WordPress 有这样的按钮，但是对于像这样特别糟糕的错误，这是一个有用的功能。一些用户抱怨说，即使他们禁用了自动更新，还是安装了这个更新。这是一条很好的路线，但似乎 WordPress 应该在设置中明确这项功能的存在，并包括一种选择退出像这样的强制更新的方式。