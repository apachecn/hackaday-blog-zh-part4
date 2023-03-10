# 本周安全:津布拉 RCE，路由器受到攻击，以及网络组装中的老把戏

> 原文：<https://hackaday.com/2022/07/01/this-week-in-security-zimbra-rce-routers-under-attack-and-old-tricks-in-webassembly/>

在`unrar`实用程序中有一个问题，因此，[Zimbra 邮件服务器很容易受到远程代码执行](https://blog.sonarsource.com/zimbra-pre-auth-rce-via-unrar-0day/)的攻击，只需发送一封电子邮件。首先，`unrar`是一个由 RarLab 开发的源代码可用的命令行应用程序，RarLab 就是 WinRAR 的开发者。 [CVE-2022-30333](https://nvd.nist.gov/vuln/detail/CVE-2022-30333) 是那里的漏洞，这是一个经典的路径遍历对档案提取。通常完成这种攻击的方法之一是提取一个指向预定目的地的符号链接，然后指向一个应该被限制的位置。`unrar`有针对这种攻击的代码硬化，但是被它的跨平台支持破坏了。在 Unix 机器上，检查存档文件中是否有任何包含`../`模式的符号链接。检查完成后，运行一个函数将所有 Windows 路径转换为 Unix 符号。因此，简单的绕过是使用`..\`遍历来包含符号链接，它不会被检查捕获，然后被转换到工作目录。

这已经够糟了，但是 Zimbra 通过自动提取收到的电子邮件中的`.rar`附件来运行病毒和垃圾邮件检查，让情况变得更糟。这种提取不是沙箱化的，所以攻击者的文件可以写在文件系统中`zimbra`用户可以写的任何地方。不难想象这将很快变成一个完整的 RCE。如果你有一个基于 RarLab 代码的`unrar`二进制文件，检查他们的二进制文件版本 6.1.7 或 6.12。虽然 Zimbra 是专门调用的应用程序，但也可能存在其他利用该应用程序的情况。

## 路由器恶意软件

在一个有点奇怪的地方发现了一个广泛传播的恶意软件活动:[运行在小型办公室/家庭办公室(SOHO)网络设备的固件上](https://arstechnica.com/information-technology/2022/06/a-wide-range-of-routers-are-under-attack-by-new-unusually-sophisticated-malware/)。令人惊讶的是，该活动支持了多少不同的设备，包括思科、网件、华硕等。关键是恶意软件是为 MIPS 架构编译的一点点二进制，很多路由器和接入点都使用 MIPS 架构。

一旦就位，恶意软件就会对 DNS 和 HTTP 连接发起中间人攻击，所有这些攻击的目标都是危害通过被危害的设备运行连接的 Windows 机器。过去曾有过大规模的攻击活动，其中 DNS 解析器在易受攻击的路由器上被修改，但这次似乎更加复杂，导致研究人员怀疑这可能是一次国家支持的活动。在来源报告的[中有一个奇怪的注释，最初的漏洞脚本调用了`/cgi-bin/luci`，这是 OpenWRT 路由器的 web 接口。我们已经从 Lumen 那里获得了更多信息，请继续关注细节。很有可能这个恶意软件活动是专门针对那些非常旧的、脆弱的基于 OpenWRT 的路由器的。多家公司使用旧版本的开源项目作为他们的 SDK 可能会有不利的一面。](https://blog.lumen.com/zuorat-hijacks-soho-routers-to-silently-stalk-networks/)

## WebAssembly 和老把戏

浏览器领域最近出现的最有趣的概念之一是 WebAssembly。你有一个用 C 写的库，想在浏览器中用 JavaScript 来使用它？将它编译成 WebAssembly，你就有了一个比 JavaScript 更快、比传统编译的二进制文件更容易使用的解决方案。这是一个非常聪明的解决方案，并允许一些疯狂的壮举，如浏览器中的谷歌地球。在浏览器中运行 C 会有什么负面影响吗？Grav 的优秀员工有一个可能出错的例子:[优秀的老缓冲区溢出](https://blog.protekkt.com/blog/basic-webassembly-buffer-overflow-exploitation-example)。

现在，它与标准溢出漏洞利用的工作方式略有不同。一个原因是，Wasm 没有地址布局随机化或数据执行保护。另一方面，web 程序集函数并不驻留在内存地址中，而只是一个函数索引。`RET`指令等价物不能跳转到任意位置，只能跳转到函数索引。然而，它仍然是一个堆栈，缓冲区溢出会导致重要数据被覆盖，比如返回指针。时间会告诉我们 WebAssembly 漏洞利用是会成为一件大事，还是永远是一件新鲜事。

## Intune 远程管理

在我们崭新而美好的未来，远程工作似乎成了新的标准，这带来了一些新的安全问题。例子:[微软的 Intune 远程管理套件](https://www.cyberis.com/article/intune-hacking-when-wipe-not-wipe)。这应该是一种远程部署、管理和监控笔记本电脑和台式机的简单方法。理论上，结合 Bitlocker 的健壮的远程管理套件应该能够有效地防止篡改。为什么选择 Bitlocker？虽然它可以防止攻击者从磁盘读取数据，但也可以防止篡改。例如，有一个非常老的技巧，在粘滞键或可访问性二进制文件的顶部复制`cmd.exe`二进制文件。这些可以从登录页面启动，并产生一个超级简单的根 shell。Bitlocker 可以防止这种情况。

听起来很棒，但是有个问题。Intune 有两种部署方式。“用户驱动”流程导致系统将更多管理功能委托给最终用户，包括访问 BitLocker 恢复密钥。唯一的解决方法是进行设置，然后删除主要用户并轮换 Bitlocker 密钥。然后是故障排除模式，在初始设置过程中按住 Shift+F10 向最终用户授予系统访问权限。呀。最后，要注意的最后一个问题是，远程擦除会删除用户数据，并从一些重要的地方删除额外的二进制文件，但不会进行任何类型的文件验证，因此我们简单的粘滞键攻击将会继续存在。哦。

## 比特和字节

[Jack Dates]参加了 2021 Pwn2Own，[组织了一个苹果 Safari 漏洞利用，该漏洞利用了英特尔图形内核扩展用于 escape](https://blog.ret2.io/2022/06/29/pwn2own-2021-safari-sandbox-intel-graphics-exploit/) 。这是对 OSX 剥削的一个非常深入的探究。立足点是长度检查中的一个错误，总共允许写入四个字节的任意数据。把它变成有用的东西的关键是在内存周围散布一些尸体——分叉的、死的进程。破坏尸体的大小，你可以用它来释放其他仍在使用的内存。免费后使用，赢取大奖！

我们上周谈到的 OpenSSL 漏洞仍在调查中，[由【Guido Vranken】负责](https://guidovranken.com/2022/06/27/notes-on-openssl-remote-memory-corruption/)。他在 5 月份发现了一个独立的 bug，该 bug 并不是一个安全问题，它是对引入我们感兴趣的 AVX512 问题的 bug 的修复。这里看起来仍然有 RCE 的潜力，但至少它被证明是不平凡的，把这样的攻击放在一起。

有一个新的恶意软件活动，yt stealler，明确针对 YouTube 帐户凭证。该恶意软件作为流行工具的虚假安装程序进行分发，如 OBS Studio、Auto-Tune，甚至欺骗和破解其他软件。运行时，YTStealer 会寻找一个身份验证 cookie，登录到 YouTube Studio，并从连接的帐户中获取所有可用的数据。这些信息和 cookie 被加密并发送到 T2 的服务器上。尚不清楚为什么 YouTube 帐户对攻击者如此感兴趣，但也许我们都可以期待垃圾视频被上传到我们最喜欢的频道。

最后，因为安全不仅仅是计算机的问题，[LockPickingLawyer](https://www.youtube.com/watch?v=OFvTzppfJnA)提供了一个令人愉快的谜题解答。洛基是一把由真正的挂锁制成的密码锁，它引起了我们最喜欢的开锁人的注意，他试图打开它。我们不会破坏任何结果，但如果拼图或锁是你的果酱，它值得一看。

 [https://www.youtube.com/embed/OFvTzppfJnA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/OFvTzppfJnA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

