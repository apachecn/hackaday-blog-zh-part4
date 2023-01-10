# 本周安全:伊朗的 ITG18、Linux 的 ProcMon 和垃圾收集失败

> 原文：<https://hackaday.com/2020/07/24/this-week-in-security-irans-itg18-procmon-for-linux-and-garbage-collection-fail/>

即使是顶级的安全专家也会犯灾难性的错误，这一次是伊朗 ITG18 的操作员。我们再一次谈论国家支持的黑客的奇怪的阴暗的世界。这个故事来自 IBM X-Force 事件响应情报服务(IRIS)。我怀疑一个死池迷一定在 IBM 工作，但这是题外话。

[一台疑似 ITG18 使用的服务器配置不正确](https://securityintelligence.com/posts/new-research-exposes-iranian-threat-group-operations/)，当数据和训练视频存储在那里时，这些数据是可以公开访问的。在捕获的数据中，有属于美国和希腊军事人员的被侵入账户的记录。

培训视频还包含一些有趣的花絮。如果目标帐户使用双因素身份验证，攻击者将记下并放弃对该帐户的访问。如果一个谷歌账户被攻破，做法是从谷歌外卖开始，谷歌外卖服务允许下载谷歌收集的与该账户相关的所有数据。约克斯。

### 要从零开始开发，你必须首先发明宇宙

我们在本专栏中已经讨论了许多内核级的漏洞，但是我们从来没有讨论过像 Secfault Security 刚刚发布的指南。他们试图在开发人员和漏洞作者之间架起一座桥梁，带领我们在 Google Project Zero 的基础上构建一个实际可行的漏洞 PoC。

### ProcMon

![ProcMon in action](img/455e2a4a481587bd07c5360c898a9e04.png)

Image by Microsoft, Licensed MIT

微软正在继续发展他们的 Linux 业务，这一次是通过将 Process Monitor 重新设计为 Linux 的 ProcMon。回顾一下历史，Process Monitor 是 Sysinternals 套件的一部分，最初由 Winternals 的创始人[Bryce Cogswell]和[Mark Russinovich]开发。顺便提一下，他们还[利用 sysinternals 工具打破了索尼 BMG rootkit 的故事](https://web.archive.org/web/20051231142359/http://www.sysinternals.com/blog/2005/10/sony-rootkits-and-digital-rights.html)。这个故事发生后不到一年，Winternals 被微软收购，虽然[Cogswell]已经离开，但[Russonovich]仍留在微软，现在是 Azure 的 CTO。

ProcMon 是用 C++编写的，在 MIT 许可下发布。它实时跟踪机器上发生的系统调用，给出系统活动的详细信息。它对于安全性、调试和解决性能问题非常有用。总而言之，这是一个非常方便的工具，应该是系统管理员工具箱中有用的一部分。该源代码是在 OSI 许可下提供的，所以各种发行版应该很快就会获得并打包 ProcMon。

### Windows 服务器容器

Windows Server 支持在容器中运行进程的几种方式:HyperV 容器和 Windows Server 容器。基于虚拟化的容器化提供了更安全的隔离，这一点已被广泛接受。也就是说，与基于内核的容器化相比，如果虚拟化容器被破坏，攻击者迁移出并攻击主机的难度要大得多。

这是一种逃离 Windows 服务器容器的新方法。虽然不像在 Linux 机器上那样经常遇到，但 Windows 确实支持符号链接。通过深入阅读还可以清楚地看到，现代 Windows 机器正在成为一种在其上具有 Windows 兼容层的 POSIX 机器。例如，“C:”目录实际上是指向“\Device\HarddiskVolumeX”的全局符号链接。

如果一个容器化的进程可以创建一个全局符号链接，也就是指向根目录的符号链接，那么容器转义将是微不足道的。正如所料，容器安全控制不允许隔离的进程在运行时创建这样的符号链接。也就是说，有一个特定的函数可以被滥用来创建全局符号链接。具体的功能参数还有待披露，以便使野外开发更困难一点。

### 密码重置出错

本周，一个网站安全审计的故事引起了我的注意，这个故事是由麦克斯韦·ꓘ·杜林整理的。密码重置表单是这里的重点，它有几个问题。第一个是常见的缺陷:密码重置表单验证给定的电子邮件地址是否在系统中。这不是最糟糕的缺陷，但它确实给了攻击者信息——他可以猜测电子邮件地址，并在有帐户使用该地址时得到确认。

下一个缺陷比较微妙，密码重置电子邮件的内容是使用 HTTP 请求中发送的主机生成的。这通常如预期的那样工作:用户进入`ourwebsite.com/reset`，输入他们的电子邮件地址，并提交表单以生成密码重置请求。他们会收到一封电子邮件，里面有一个返回到`ourwebsite.com`的链接，允许他们重置密码。但是，攻击者可以使用他人的地址向密码重置表单发送恶意的 HTTP 请求，并操纵主机值。重置电子邮件现在指向注入的主机。如果用户单击电子邮件中的链接，魔值将被发送到攻击者指定的主机，然后攻击者可以重置用户的密码。

麦克斯韦发现的最后一个缺陷是所有缺陷中最糟糕的。当用户第一次点击通过电子邮件发送的链接时，重置令牌会被确认，但当密码实际更新时，它不会被确认。您可以创建自己的帐户，完成密码重置过程，然后将密码重置表单更改为指向另一个用户的帐户。因为后端认为您已经通过了身份验证，所以它会尽职尽责地设置新密码，即使指定的帐户不是您的。

我们中没有人会使用这个进行审计的小网站，但是描述的步骤和要寻找的问题对任何需要做同样事情的人来说都是一个很好的指导。

### 免费后使用垃圾收集

[CVE-2019–1367 在这一点上是一个更老的 bug](https://blog.confiant.com/internet-explorer-cve-2019-1367-in-the-wild-exploitation-prelude-ef546f19cd30)，在 2019 年被发现在野外被利用，并由 Confiant 给出了完整的报道。这是 Internet Explorer 引擎中的又一个漏洞。简单回顾一下，`jscript.dll`是不推荐使用的 Javascript IE 实现。它不再是默认的实现，但是出于兼容性的目的，可以被网页请求。看来`jscript.dll`只能在 Internet Explorer 中访问，Edge 的两个版本都不支持传统实现。

这个 vuln 被国家行为者积极使用，是一种水坑式攻击，只要访问恶意站点就足以危及安全。报道的下一页[介绍了技术细节。这是我们以前没有涉及过的一类漏洞。在垃圾收集语言中，这是一种先用后免的用法。](https://blog.confiant.com/internet-explorer-cve-2019-1367-exploitation-part-1-7ff08b7dcc8b)

垃圾收集是手动释放内存的替代方法。其中一个优点是，它应该使释放后使用错误成为过去，那么这里发生了什么呢？在某些情况下，`jscript.dll`中的垃圾收集代码不能正确跟踪引用计数。这个 bug 专门处理`Array.sort()`回调函数。该函数的参数没有被正确跟踪，因此可以操纵 JS 实例，以便 GC 清扫释放一个稍后将被访问的对象。

关于这个漏洞如何在野外使用的利用和进一步分析，请查看完整报道的[第 2 部分](https://blog.confiant.com/internet-explorer-cve-2019-1367-exploitation-part-2-8143242b5780)和[第 3 部分](https://blog.confiant.com/internet-explorer-cve-2019-1367-exploitation-part-3-a92d3011b38)。