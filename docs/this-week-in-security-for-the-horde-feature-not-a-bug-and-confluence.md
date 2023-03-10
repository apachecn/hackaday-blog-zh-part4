# 本周在安全:对于部落，功能没有一个错误，并汇合

> 原文：<https://hackaday.com/2022/06/10/this-week-in-security-for-the-horde-feature-not-a-bug-and-confluence/>

如果你回溯开源 webmail 项目的历史，你会发现 Horde，一个群件 web 应用程序。它于 1998 年首次在 Freshmeat 上发布，2012 年初，当人们发现 3.0 版本被篡改，包含后门的软件包已发货三个月时，它获得了一些恶名。虽然这一次不是有意的后门，但在 Horde 网络邮件接口中有一个非常严重的问题。或者更准确的说，是一对问题。最严重的是 CVE-2022-30287，这是一个 RCE 漏洞，允许经过验证的用户在连接的服务器上触发代码执行。

易受攻击的元素是 Turba 地址簿模块，它使用 PHP 工厂方法来访问特定的地址簿。`create()`方法有一段有趣的代码，它首先检查初始值。如果是一个字符串，该值被理解为要访问的本地地址簿的名称。但是，如果工厂是用数组初始化的，任何地址簿驱动程序都可以使用，包括 IMSP 驱动程序。IMSP 从远程服务器获取序列化数据，并对其进行反序列化。是的，PHP 可能有反序列化错误，这个在主机上运行代码。

不过也没那么差，只是认证用户吧？这已经够糟了，但是第二个错误是跨站点请求伪造，CSRF，由查看电子邮件触发。因此，在易受攻击的部落服务器上，任何用户查看恶意信息都会触发服务器上的 RCE。哦。所以让我们来谈谈修复。有一个新版本的 Turba 模块似乎可以修复这些错误，但不清楚实际的 Horde 套件是否已经推出了包含它的更新。所以你可能要靠自己了。正如发现漏洞的 Sonar 博客所指出的那样，在这一点上，Horde 本身似乎基本上没有得到维护。也许是时候考虑迁移到一个更新的平台了。

### 漏洞还是特性？

微软对 Follina 的处理还在继续。还有另一个类似的问题:[走狗](https://blog.0patch.com/2022/06/microsoft-diagnostic-tools-dogwalk.html)。它不像 Follina 那么糟糕，这是一个在`.diagcab`处理中的问题。cab 可以指向远程 WebDAV 服务器上的 XML 文件，返回的文件会绕过对不允许的文件名的正常检查。例如，`\..\..\..\..\..\..\..\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Startup\malicious.exe`被创造出来，带来了可预见的灾难性后果。

现在，这是一个漏洞吗？一方面，它是用户有意打开的从互联网下载的文件。另一方面，它不是一个可执行文件，不应该运行任意代码。web 浏览器会很乐意下载并让用户运行潜在的恶意文件。这不是 10.0，但听起来像一个漏洞。微软拒绝发布 CVE，类似于他们最初对 Follina 的处理，这仍然是一个未打补丁的 0 天漏洞，正在被大肆利用。我们可以推测微软已经收到了一封关于这个漏洞的国家安全信函，但是这种可能性微乎其微。

### 另一个没有的弱点

或者这是一个弱点。你决定吧。这个强大的库是 Node.js 库，用于解析表单数据，包括文件上传。该漏洞是 [CVE-2022-29622](https://nvd.nist.gov/vuln/detail/CVE-2022-29622) ，一个任意文件上传问题。你可能已经看到了那里的争论。通过设计，文件上传库允许任意上传。这实际上是图书馆的一个特色。整个漏洞报告也是如此，得分 9.8，完全是胡扯？不，实际上是有一个 bug——或者至少有一个特性并不总是像预期的那样运行。

当你使用 calendar 上传文件时，它会用一个随机的十六进制字符串替换文件名。有一个保持文件扩展名的选项，所以如果你上传`example.txt`，你会在服务器上得到一个名为`84d38f5e070c248df3cdccc00.txt`的文件。问题是文件名中有多少被认为是扩展名。第一个句点之后的所有内容都被视为扩展名，这意味着如果您上传了一个名为`test.pdf.jqlnn⟨img src="a"⟩.png`的文件，您将获得一个名为`randomstring.pdf.jqlnn⟨img src="a"⟩.png`的文件。如果你依靠这种安排来净化上传的文件名，你可能会得到一个 XSS 甚至 RCE 奖。但这并不是强大的弱点。

这是[【z solt Imre】在对](https://medium.com/@zsolt.imre/is-cybersecurity-the-next-supply-chain-vulnerability-9a00de745022)问题的分析中提出的论点，[进一步辩护](https://medium.com/@zsolt.imre/cve-2022-29622-in-vulnerability-analysis-5cf783c3721)。真正的问题是，仓促的修复[引入了一个至少和它试图修复的问题同样严重的问题。](https://github.com/node-formidable/formidable/issues/862)

### 剥削下的合流

亚特兰蒂斯的汇流有一个关键的未经认证的 RCE 正在被开发利用。Volexity 的研究人员在调查了一对被入侵的服务器后，披露了这个故事。[攻击的样本已经在各种蜜罐中被捕获](https://www.pwndefend.com/2022/06/08/learn-to-soc-java-webshell-via-confluence/)，这看起来像是一个简单的漏洞利用。由于 confluence 服务器的性质，这个问题有可能产生后续影响，因为攻击者已经进入了开发者网络。

### 比特和字节

把 RDP 暴露在互联网上有多可怕？对于这些 Linux 老手来说，暴露 SSHD 更可怕。4 天后，他们记录了近 40，000 次尝试，其中大多数都是针对管理员帐户的。同样有趣的是有多少攻击来自一对网络地址块，45.227.254.0/24 和 194.165.16.0/24，这两个地址块都属于 Flyserver。

在运营了 10 多年后， [SSNDOB 市场被下线](https://arstechnica.com/tech-policy/2022/06/feds-seize-ssndob-marketplace-that-listed-personal-data-of-24-million-people/)。这个组织[可能是殴打布莱恩·克雷布斯的幕后黑手。](https://arstechnica.com/information-technology/2013/03/security-reporter-tells-ars-about-hacked-911-call-that-sent-swat-team-to-his-house/)唯一不幸的是，此次行动中没有逮捕任何人。