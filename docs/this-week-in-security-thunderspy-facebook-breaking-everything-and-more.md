# 本周安全:雷霆间谍，脸书打破一切，等等

> 原文：<https://hackaday.com/2020/05/15/this-week-in-security-thunderspy-facebook-breaking-everything-and-more/>

Thunderspy 本周发布，由[bjrn Ruytenberg]开发。对雷电 3 协议的一系列攻击，Thunderspy 是盗梦空间、PCILeech 和 Thunderclap 风格的下一个漏洞。

《盗梦空间》和 [PCILeech](https://github.com/ufrisk/pcileech) 是对 Firewire、Thunderbolt 1 和 PCIe 内置的简单直接内存访问(DMA)的攻击。设备可以通过链路连接并请求 DMA。一旦被授予权限，它就可以访问最底层的 4gb 系统内存，既有读写权限。不难想象这将是一个巨大的安全问题，而且似乎这种技术在被发现时已被情报机构使用。另外，硬件 DMA 完全独立于软件，因此可以通过 firewire 调试崩溃的内核。

一旦漏洞被公开，硬件和软件供应商已经采取措施来加强他们的系统抵御攻击。Thunderbolt 2 引入了安全级别来缓解攻击。在向设备提供 DMA 之前，用户必须将设备标记为可信。Thunderclap 利用了单个操作系统如何与这些硬件缓解措施交互的一系列漏洞。

![](img/3d304d2ebd12bcb285e897c33c6a3886.png)

Image by Björn Ruytenberg. Licensed under CC BY 4.0.

现在，Thunderspy 滥用了英特尔雷电 3 规范和实现中的一系列问题。一个有趣的攻击是克隆一个已经被信任的 Thunderbolt 设备。将 Thunderbolt 设备插入 Linux 机器很容易捕获设备 UUID。恶意 Thunderbolt 设备可以被赋予相同的 UUID，并突然具有与克隆设备相同的信任级别。

[bjrn]将攻击推进了一步，发现他可以拆卸笔记本电脑或 thunderbolt 设备，并直接从 thunderbolt 控制器上读取固件。该固件可以被修改和重新上传。最简单的攻击之一是将安全级别设置为最低。

这是一项有趣的研究，并且已经有修复方法来减轻所发现的问题。真正的问题是 Thunderspy 有多重要。威胁模型是邪恶的女仆:留在汽车旅馆房间里的笔记本电脑会在几分钟内被清洁人员使用。Thunderspy 可能会被用于这种类型的攻击，但还有许多其他潜在的更好的攻击选项。在一个狭窄的环境中，Thunderspy 是一种完美的技术:一个带有加密驱动器的设备，它已经通电并登录，但被锁定。在这种情况下，Thunderspy 可以用来恢复存储在内存中的驱动器加密密钥，然后用来植入恶意软件。

### 那次脸书打破了一切

6 号你可能已经注意到了一些普遍的 iOS 应用行为不端。脸书对他们的登录 SDK 的服务器组件进行了更改，这导致许多使用该 SDK 的应用程序崩溃。值得一问的是，这么多受欢迎的应用程序使用脸书代码是否是一个好主意。除了拒绝服务之外，似乎没有其他漏洞或危害途径。

### 大规模 WordPress 攻击

在一场针对各种漏洞的运动中，近一百万个 WordPress 网站受到攻击。一般的攻击策略是注入一个恶意的 javscript，它处于休眠状态，直到被站点管理员执行。具有讽刺意味的是，登录您的网站检查是否有危害可能是导致危害的导火索。像往常一样，让你的插件保持最新，并遵循其余的最佳实践。

### Godaddy 违约

Godaddy 用户最近被告知[有一个漏洞，暴露了他们的部分帐户以危及](https://www.bleepingcomputer.com/news/security/godaddy-notifies-users-of-breached-hosting-accounts/)。值得注意的是，妥协发生在 2019 年 10 月，6 个月后才被发现。Godaddy 表示，除了最初的妥协之外，没有任何恶意行动的证据，这本身就令人费解。

> 2020 年 4 月 23 日，我们发现 SSH 用户名和密码在我们的托管环境中被篡改了。这影响了大约 28，000 名客户。我们立即重置了这些用户名和密码，从我们的平台上删除了违规的 SSH 文件，并且没有迹象表明威胁参与者使用了我们客户的凭据或修改了任何客户托管帐户。需要明确的是，威胁者没有权限访问客户的主要 GoDaddy 帐户。

### 漏洞利用

一个有趣的 [RCE 漏洞被发现](https://frichetten.com/blog/cve-2020-11108-pihole-rce/)在 Pi-hole 软件中。这个特殊的问题需要对整个管理 web 界面进行认证访问，所以它本身不太可能引起太多问题。利用这个漏洞很简单，只需将`[http://192.168.122.1#](http://192.168.122.1#)" -o fun.php -d "`设置为远程阻止列表，并使用您控制的 IP。在幕后，远程阻止列表是通过 curl 获取的，url 没有经过适当的清理。您的 PHP 代码保存在 web 目录中，一个 HTTP 请求触发该代码。

### Github 上的泄漏

[Tillson Galloway]讲述了[如何通过在 Github 中搜索不应该存在的密码和密钥，获得 1 万美元的 bug 奖金](https://tillsongalloway.com/finding-sensitive-information-on-github/index.html)的故事。通过搜索特定的关键词，他发现了各种有趣的、无意的东西。`vim_settings.xml`包含最近复制和粘贴的字符串，`.bash_history`包含已经运行的命令的记录。有多少次你不小心在命令行中输入了密码，以为你在用 SSH 或 sudo 进行身份验证，这只是一个例子？这是一个很容易犯的错误，意外地将这些隐藏文件中的一个包含在公共存储库中。

曾经有过 API 密钥意外包含在源代码 drops 中的例子，甚至多年来 SSL 证书也是这样泄露的。这对我们所有人都是一个教训，确保在将代码推送到 Github 之前清理项目。