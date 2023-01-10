# 本周安全:Nvidia，勒索软件退休，以及 Docker 中的 TOCTOU Bug

> 原文：<https://hackaday.com/2019/06/07/this-week-in-security-nvidia-ransomware-retirement-and-a-toctou-bug-in-docker/>

Nvidia 的 GeForce Experience (GFE)是 Nvidia 驱动程序的配套应用程序，可以使所述驱动程序保持最新，并添加有关直播和媒体捕捉的功能。该应用程序作为两个部分运行，一个 GUI 和一个系统服务，使用 HTTP API 进行通信。来自 Rhino Security Labs 的[David Yesland]决定研究这个 API，寻找有趣的、未记录的行为，并在 2 日周日[分享了结果](https://rhinosecuritylabs.com/application-security/nvidia-rce-cve-2019-5678/)。

第一个有趣的发现是，该服务是用 Javascript 编写的，并使用 Node.js 运行。Javascript 是一种脚本语言，而不是编译语言——该服务的源代码是开放供研究的。这揭示了只要请求包含适当的安全令牌，任何来源的 API 请求都可以被接受。该应用程序包括一个更新机制，允许授权的 API 调用执行任意系统命令。只要身份验证令牌没有泄露给攻击者，这仍然不是问题，对吗？

现代浏览器包括一种用任意文本填充剪贴板的机制。每当你“点击此处复制到剪贴板”时，你已经使用过它。也可以从 javascript 启动文件上传对话框。研究人员建议的利用方法是欺骗用户使用 ctrl+v 组合键，然后是 enter 键。也许是一个对话框，要求某人将参考号粘贴到字段中，然后按 enter 继续。实际发生的情况是，页面会检测到控制键击，用安全令牌的位置填充剪贴板，并启动文件上传对话框。用户按“v”，将剪贴板的内容粘贴到对话框中，最后“Enter”开始文件上传。一旦攻击者获得安全令牌，就可以向本地 API 发出 HTTP 请求，启动任意命令。

Nvidia 意识到了这个潜在的问题，发布了一个补丁，并发布了一个关于这个问题的安全公告。[David]承认修复，但指出潜在的问题仍然存在，即允许来自任何来源的 API 请求。他建议不经常使用 GFE 的人卸载它。

### 勒索软件即服务退役

GandCrab 是一个勒索软件即服务(RaaS？)自 2018 年初以来一直像企业一样运营的产品。它有一个在线店面，罪犯可以在那里订阅服务并获得定制的恶意软件。RaaS 作者从支付的赎金中抽取一小部分。显然，GandCrab 的生意做得很好，因为他们宣布退休。他们声称，在经营这项非法服务的一年半时间里，他们已经赚了超过 1.5 亿美元，现在“……准备退休，这是他们应得的。我们已经证明，通过做坏事，报应不会到来。”

尽管这种大胆令人钦佩，但细节可能并不完全可信。像这样的声明，尤其是在运行勒索软件服务之后，给那些负责任的人描绘了一个相当大的目标。时间会证明这种大胆是否合理。

### 触地得分

Docker 可以说是让容器化重新流行起来的项目。基于 Docker 的解决方案比完整的虚拟机更高效，同时拥有几乎相同的安全优势，因此特别有用。[一个时间检查使用时间(TOCTOU)漏洞](https://seclists.org/oss-sec/2019/q2/131)最近被【Aleksa Sarai】发现。在 docker 函数 FollowSymlinkInScope 中，恶意创建的 docker 映像可能会在 Docker 复制操作期间读取和写入主机上的任何文件。

[![](img/3e0dc3c8a0c03e6601b3da0a8a820a3f.png)](https://hackaday.com/wp-content/uploads/2019/06/qwe_download.jpg)

There seems to be a tshirt for [everything](https://teespring.com/cond?pr=10off)

我们从来没有在 Hackaday 上讨论过 TOCTOU bugs，所以有必要先介绍一下。标准发音似乎是“TOCK too ”,尽管拼写缩写也是可以接受的。例如，FollowSymlinkInScope 采用一个给定的路径，并验证任何符号链接是否指向 docker 映像中的位置，纠正任何本来会指向主机系统的符号链接。那是托克托的“支票”。路径被安全地解析，并最终用于将文件复制到正确的位置，即“Use”元素。这里的关键是运行检查和利用路径之间的时间跨度。攻击者基本上可以与该时间间隔赛跑，在检查完成后对磁盘上的符号链接进行更改。TOCTOU 的基本缺陷是假设一旦某个元素被检查，它将保持相同的状态，直到采取行动。

为了理解为什么 TOCTOU 错误难以修复，我们必须考虑现代多任务处理以及原子操作是如何工作的。在单核处理器中，当其他程序运行时，程序会不断暂停。这个想法可以追溯到 20 世纪 70 年代的第一个分时系统。现代多核处理器加剧了潜在的问题，因为进程可以同时运行，所有进程都对同一个文件系统进行更改。原子操作是一次完成的操作，在它完成之前，没有任何其他进程能够观察或修改它。不同的操作系统和架构提供了不同的原子函数集，使得 TOCTOU 错误很难避免。对于 docker 问题，[Aleksa]提出了一个新的内核函数，允许自动解析 Docker 映像中的符号链接。在这种情况下，由于内核将净化步骤作为访问文件的一部分来执行，操作将变成原子性的。

### 记事本和 RDP

当一名研究人员发现一个漏洞并编写一份概念证明时，发射的有效载荷通常是 calc.exe 或 notepad.exe。[塔维斯·奥曼迪]发现了记事本本身的一个漏洞，彻底颠覆了这一传统。在 90 天内，或者一旦微软修复了这个问题，我们将确保向您提供故事的其余部分。

我们几周前报道的 RDP 漏洞，即 [Bluekeep](https://hackaday.com/2019/05/21/this-week-in-security-whats-up-with-whatsapp-windows-xp-patches-and-cisco-is-attacked-by-the-thrangrycat/) ，是一个持续发生的故事。补丁正式发布两周后，masscan fame 的[Robert Graham]扫描了整个互联网，寻找易受攻击的 RDP 服务。他发现了至少 90 万台易受攻击的机器。也就是说，RDP 接触到互联网的近 100 万台 Windows 电脑还没有安装安全补丁。这就是为什么微软认为 Bluekeep 是一个如此大的问题。