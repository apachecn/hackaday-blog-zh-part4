# 主要 Bug 授予所有主要 Linux 发行版的 Root 权限

> 原文：<https://hackaday.com/2022/01/26/major-bug-grants-root-for-all-major-linux-distributions/>

选择 Linux 作为操作系统的主要原因之一是它比 Windows 安全得多。这有很多原因，包括适当的用户权限、从可信来源安装软件，当然，事实上大多数 Linux 软件包括 Linux 内核本身都是开源的，允许任何人查看代码的漏洞。然而，这并不意味着 Linux 是绝对安全的，因为[研究人员最近发现了一个在大多数主要 Linux 发行版中发现的重大缺陷，它允许任何人以根用户](https://www.bleepingcomputer.com/news/security/linux-system-service-bug-gives-root-on-all-major-distros-exploit-released/)的身份运行代码。

该漏洞是 Polkit 中的一个内存损坏漏洞，pol kit 是一个处理各种系统进程特权级别的框架。它特别影响了程序`pkexec`。有了[概念验证漏洞利用](https://haxx.in/files/blasty-vs-pkexec.c)(文件下载警告)，攻击者要升级到 root 用户，只需在计算机上编译程序，并作为默认用户运行。[Jim MacDonald 在 Twitter](https://twitter.com/os2mac/status/1486145352742801414) 上为那些不愿意在自己的机器上尝试的人展示了一个例子。

虽然听起来很糟糕，但似乎所有受此影响的主要发行版都已经发布了修补该问题的更新，包括 Debian、Ubuntu、Red Hat、Fedora、open SUSE 和 Arch。还有一个临时的解决方法，从`pkexec`程序中删除读/写权限，这样它就根本不能运行了。也就是说，最好检查一下你的 Linux 系统是否都是最新的，并且最近没有陌生人在终端中输入随机命令。