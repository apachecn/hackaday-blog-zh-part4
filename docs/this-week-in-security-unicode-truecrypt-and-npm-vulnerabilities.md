# 本周安全:Unicode、Truecrypt 和 NPM 漏洞

> 原文：<https://hackaday.com/2019/12/20/this-week-in-security-unicode-truecrypt-and-npm-vulnerabilities/>

Unicode 是对 ASCII 的精彩扩展，它为我们提供了像“✈”、“⌨”和“☕”这样的珍宝，它有一些意想不到的安全后果。Unicode 最常见的问题是视觉安全问题，比如字母之间的字符混淆。例如，英文“M”(U+004d)与西里尔文“м”(U+041 c)难以区分。你能说出 IBM.com 和 IBМ.com 的区别吗？

这个由[John Gracey]发现的 bug 彻底改变了常见的问题[。恰当地称为大小写映射冲突，它是不同的 Unicode 字符被映射到相同的大写或小写字母的故事。](https://eng.getwisdom.io/hacking-github-with-unicode-dotless-i/)

`'ß'.toLowerCase() === 'SS'.toLowerCase() // true
// Note the Turkish dotless i
'John@Gıthub.com'.toUpperCase() === 'John@Github.com'.toUpperCase()` 

GitHub 以小写形式存储所有电子邮件地址。当用户发送密码重置时，GitHub 的逻辑是这样工作的:获取请求密码重置的电子邮件地址，转换为小写，并查找使用转换后的电子邮件地址的帐户。这本身没有问题，但是重置信息会被发送到所请求的电子邮件地址，而不是文件上的那个。回想起来，这是一个明显的缺陷，但是如果没有 Unicode 的存在和大小写映射冲突的可能性，这将是一个非常安全的实践。

这个缺陷似乎在很久以前就被修复了，但是最近才被披露。这也是一个我们没有涉及的影响 Unicode 的新问题。有趣的是，我的研究发现，早在 2013 年，Spotify 就出现了几乎相同的问题。


### TrueCrypt 和德国秘密

TrueCrypt 是一款神奇的软件，它改变了世界，为每一个计算机用户提供了一个免费的、源代码可用的硬盘加密解决方案。虽然该程序的源代码是免费提供的，但许可证是奇怪的，限制性的，从技术上讲，它既不是自由软件，也不是开源软件。这使得它没有被包括在许多主要的操作系统发行版中。即便如此，TrueCrypt 已经被许多人使用，而且出于许多原因，从无辜的人到应受谴责的人。TrueCrypt 非常受欢迎，一项众筹活动筹集了足够的资金，在 2013 年对 TrueCrypt 代码进行了专业审计。

故事在源代码审计的中途发生了奇怪的转折。就在最初的审计结束后，就在深入的第二阶段审计开始前，TrueCrypt 开发人员突然宣布他们将结束开发。TrueCrypt 网站仍然显示公告:“警告:使用 TrueCrypt 是不安全的，因为它可能包含未修复的安全问题。”许多用户认为这个时机很奇怪，并猜测有某种后门会被审计发现。深入审计已经完成，虽然发现了一些小问题，但没有发现特别严重的问题。

TrueCrypt 更令人惊讶的用户之一是德国政府。最近发现 BSI，德国政府的信息安全部门，在 2010 年对 TrueCrypt 进行了一次审计。

许多政府现在已经有了确立信息自由的法律，赋予他们的公民“知情权”。根据这些法律，公民可以正式要求提供文件，如果存在这种文件，除少数例外，政府必须提供。一名德国公民向[发出官方请求，要求提供关于 TrueCrypt 的信息](https://translate.google.com/translate?sl=auto&tl=en&u=https%3A%2F%2Ffragdenstaat.de%2Fanfrage%2Ftrue-crypt-unterlagen-und-backdoor%2F)，特别是关于该软件中已知的后门。令人惊讶的是，这样的文档确实存在！

德国政府秘密地给 TrueCrypt 开了后门吗？他们是阴谋的一部分吗？大概不会。经过一些繁文缛节和法律上的争论，审计报告的文本最终被发布并获准出版。在 2010 年发现的一些问题仍然存在于 TrueCrypt/Veracrypt 源代码中，并在这份报告曝光后得到了修复。

### NPM 二元种植

Node Package Manager，Javascript 所有东西的心爱仓库，最近推出了一个更新，并宣布了一对漏洞。简单地说，这些漏洞都是由于在安装包时缺乏任何健全性检查造成的。

首先，二进制安装路径在安装期间没有被清理，这意味着一个包可能试图与目标文件系统上的任何文件进行交互。尤其是以 root 用户身份运行 NPM CLI 时，滥用的可能性非常大。虽然在版本 6.13.3 中解决了第一个问题，但是在该版本中仍然存在第二个类似的问题。

安装路径在 6.13.3 中被清理了，但是第二个问题是软件包可以在它的安装位置的任何其他文件上安装二进制文件。一个包本质上可以将代码注入到其他已安装的包中。对此的修复方法是只允许包覆盖该包拥有的二进制文件。

好处是用户必须安装一个受损的软件包才会受到影响。通过以非 root 用户身份运行 NPM，这种影响也大大减轻了，这似乎是一种好的做法。

### 谷歌云外壳

Google 围绕他们的云产品提供了一系列服务，并提供了非常有用的基于 web 的云 Shell 接口来管理这些服务。Offensi 的一名研究人员花了一些时间寻找漏洞，[找出了其中的 9 个](https://offensi.com/2019/12/16/4-google-cloud-shell-bugs-explained-introduction/)。第一步是识别运行环境，在本例中是一个 docker 映像。一个指向主机系统的套接字暴露在外，使得研究人员可以轻松地逃离 Docker 容器。从那里，他能够启动一些调试工具，并开始寻找漏洞。

详细描述的漏洞本身就很有趣，但我最感兴趣的是寻找和发现它们的过程。谷歌甚至赞助了一个详细介绍这项研究的 YouTube 视频，嵌入如下:

 [https://www.youtube.com/embed/E-P9USG6kLs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/E-P9USG6kLs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



### 零碎东西

[用 iPhone 攻破 Windows 机安全](https://decoder.cloud/2019/12/12/from-iphone-to-nt-authoritysystem/)？当 iPhone 插入机器时，iPhone 驱动程序设置特定文件的权限。该文件实际上可能是一个重要系统文件的硬链接，iPhone 驱动程序可能会无意中使该任意文件可写。

Nginx 网络服务器目前被劫持。显然，最初编写 Nginx 的程序员当时为一家技术公司工作，现在 Nginx 项目被收购了，那家公司声称拥有代码的所有权。这可能只是一个欺诈性的声明，但如果这一声明得到支持，其影响将是深远的。

[OpenBSD 修复了一个简单的权限提升](https://www.qualys.com/2019/12/11/cve-2019-19726/local-privilege-escalation-openbsd-dynamic-loader.txt)，其中使用一个非常奇怪的 LD_LIBRARY_PATH 调用 setuid 二进制文件——一个点和许多冒号。这诱使加载程序加载用户拥有的库，但具有 root 权限。