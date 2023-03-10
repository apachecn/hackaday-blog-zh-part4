# 本周安全:VMWare、微软团队、Python Fuzzing 等

> 原文：<https://hackaday.com/2020/12/11/this-week-in-security-vmware-microsoft-teams-python-fuzzing-and-more/>

据 NSA[称，VMWare 的一个问题正在被大肆利用。该漏洞是](https://media.defense.gov/2020/Dec/07/2002547071/-1/-1/0/CSA_VMWARE%20ACCESS_U_OO_195076_20.PDF)[管理控制台上的一个命令注入](https://www.vmware.com/security/advisories/VMSA-2020-0027.html)。支持该控制台的 web 主机显然是以 root 用户身份运行的，因为该漏洞允许“在底层操作系统上以无限制权限执行命令”

有趣的是，VMWare 从 NSA 那里了解到了这个漏洞，这似乎表明它是一个被外国使用的零日漏洞。他们列出的危害链也奇怪地具体，让我怀疑这是一个观察到的攻击的净化帐户。

## 微软团队和非 CVE 团队

[Oskars Vegeris] [在微软团队客户端](https://github.com/oskarsve/ms-teams-rce)中发现了一对有趣的问题，这两个问题一起允许一个无交互的、可蠕虫化的 RCE。第一个漏洞是 XSS 问题，其中包含“提及”的消息可以在传输过程中被修改，以包含任意 Javascript。为了让 JS 通过 XSS 保护过滤器，在有效载荷中包含了一个 unicode 空字节。第二个漏洞是使用 Teams 应用程序中的内置文件下载代码来下载并自动运行二进制文件。总之，任何人只要在他们的团队应用程序中加载消息，就可以运行代码。

Vegeris 指出，由于如此多的用户出现在多个房间中，因此利用这一漏洞来构建可以感染全球大多数团队用户的蠕虫是微不足道的。这个漏洞被私下报告给了微软，并在 10 月份被修复。一个被广泛使用的工具中的可蠕虫 RCE 似乎是一件大事，应该得到很高的 CVE 分数，对吗？微软对这一攻击链给出了两个评级，针对它可能影响的两个版本的团队。对于 Office365 客户端来说，它是“重要的，欺骗的”，这是一个 bug 所能做到的最不重要的。至少，桌面应用程序在 RCE 奖中被评为“关键”。原因似乎是沙盒逃生只适用于独立的桌面应用程序。

但是没有 CVE 发布的漏洞链。在安全社区，收集简历是你简历的重要工作证明。微软回答说，他们不会为没有用户交互就自动更新的产品发布 CVE。混乱随之而来。

## 用 atheros 起毛

Google [发布了 Atheris，一个新的开源模糊工具](https://opensource.googleblog.com/2020/12/announcing-atheris-python-fuzzer.html)，专门为 Python 程序编写。模糊化是用生成的输入(通常是被认为是畸形的输入)运行程序或库，并跟踪发生了什么的过程。近年来，许多漏洞都是通过这种方式发现和修复的。Atheris 是一个覆盖导向的 fuzzer，这意味着它跟踪每一次迭代中执行的代码行，并试图最大化覆盖的代码行。

公告文章指出了 Atheris 的一个有趣的用例——测试一个库的两个实现的 bug 对 bug 的兼容性。与浏览器版本相比，用 Python 编写的 JSON 解析器就是一个例子。您将设置一个测试运行，从有效的 JSON 开始，然后在每次迭代中稍微转换一下输入。在两个实现中运行相同的输入，然后比较输出。

不甘示弱的英特尔也刚刚发布了一款 bug 查找工具 [ControlFlag](https://newsroom.intel.com/news/intel-machine-programming-tool-detects-bugs-code) 。这个工具的工作原理非常不同，它使用机器学习来发现编写的源代码中的异常。我希望我能告诉你源代码是可以使用的，但是看起来这个工具只是被公布了，并没有公开发布。

## SSL 根证书滥用

哈萨克斯坦似乎正在从事一些奇怪的安全实践，很可能是为了[能够窥探互联网流量](https://www.zdnet.com/article/kazakhstan-government-is-intercepting-https-traffic-in-its-capital/)。首都的互联网服务提供商正在阻止对谷歌、推特等网站的访问，直到政府颁发的根证书被安装并信任在连接的浏览器中。政府称这是一次“训练演习”，但由于该证书的有效期为 20 年，这似乎是公然企图使 HTTPS MitM 攻击公众。诸如此类的故事提醒我们，像 [OCSP 钉住](https://en.wikipedia.org/wiki/OCSP_stapling)和 [DNS 认证机构授权](https://en.wikipedia.org/wiki/DNS_Certification_Authority_Authorization)这样的事情是多么重要。这两种协议扩展都旨在保护用户免受由可信根证书颁发的欺诈性证书的侵害。

## 特技机器人进化并获得新技能

Trickbot 恶意软件平台是一个集窃取凭据、控制僵尸程序和安装勒索软件于一体的工具。看起来一个新的技巧正在被添加到已经溢出的袋子中——固件修改。来自 [RWEverything](http://rweverything.com/) 的核心库已经在 Trickbot 的最近样本中被发现，并且已经观察到该恶意软件正在对机器固件进行侦察。到目前为止，还没有人观察到 Trickbot 的恶意固件写入，但这种能力现在已经存在，这就足够令人担忧了。