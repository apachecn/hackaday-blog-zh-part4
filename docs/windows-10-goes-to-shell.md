# Windows 10 去壳

> 原文：<https://hackaday.com/2019/06/10/windows-10-goes-to-shell/>

windows 10——让人爱恨交加的操作系统。即使你是一个 Linux 的死忠，它是一个公平的赌注，你的工作场所使用它，你有朋友和家人需要帮助，迫使你使用 Windows 至少有时。如果你更喜欢命令行——或者甚至只是找到一个你必须使用命令行的地方，你可能会发现经典的 Windows shell 有点苍白无力。有些是 shell 的错，但有些是 Windows 控制台的错，它是一种终端程序，运行各种基于 Windows 文本的程序。不过，如果你在 Windows 10 上有 creator update 频道，那么控制台和 Linux 系统最近有了一些改进，最终将惠及主流用户。

## 有什么新鲜事？

有什么新鲜事吗？据微软称，他们已经改进了呼叫界面，以使以下内容(以及“许多其他内容”)正常工作:

*   核心工具:apt、sed、grep、awk、top、tmux、ssh、scp 等。
*   贝壳:Bash，zsh，fish 等。
*   开发工具:vim、emacs、nano、git、gdb 等。
*   语言和平台:Node.js & npm、Ruby & Gems、Java & Maven、Python & Pip、C/C++、C# &
*   。NET Core & Nuget，Go，Rust，Haskell，Elixir/Erlang 等。
*   系统和服务:sshd、Apache、lighttpd、nginx、MySQL、PostgreSQL

对控制台的更改主要围绕转义序列、颜色和鼠标支持。API 的变化包括允许某些非管理用户创建符号链接。我们已经让 X Windows 与 Windows 一起工作(使用第三方 X 服务器)，微软承认已经完成了。然而，他们仍然不支持它。

## 为什么为什么？

Linux 或多或少遵循 Unix 操作系统提出的基本规则。虽然它随着时间的推移而发展，但 Unix 是为运行在与现代计算机没有太大区别的计算机上而构建的。诚然，PDP-7 是一台 18 位计算机，但它没有 MSDOS 成长过程中令人窒息的准 8 位架构。另一方面，MSDOS 正与相当多的硬件限制作斗争。但 MSDOS 最终得到了一个名为 Windows 的外壳。然后 Windows 反败为胜，成为可以运行 MSDOS 的操作系统。但这导致了一系列问题，尤其是壳牌公司的不景气。对此有几种答案。即使回到 MSDOS 时代，像 4DOS 这样的第三方 shell 也很流行，更不用说 Cygwin、MKS 和类似工具提供的类似 Unix 的 shell 了。现代 Windows 仍然有一个不完善的 MSDOS shell，但也有 PowerShell 和 WSL bash shell。

这种不同的传统导致了标准 shell 和最简单的 Linux shell 之间的巨大差异。当然，您可以在 Linux 上的虚拟化下运行 Windows，反之亦然。然而，这应该执行得更好，因为它本质上是反向的 [Wine](https://www.winehq.org/) (也就是说，在运行 Linux 的 Windows 上的一层，就像 Wine 是在运行 Windows 的 Linux 上的一层一样)。

## 终端速度

还有一个新的 Windows 终端应用程序来管理所有带有标签和表情符号字体支持的外壳——因为显然，这很重要。你可以在下面的视频中看到一个浮华的广告。

 [https://www.youtube.com/embed/8gw0rXPMMPE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/8gw0rXPMMPE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



从拥有如此多的基于浏览器的应用程序到现在几乎在所有东西上都有 bash shell，您几乎不需要关心使用什么 CPU，甚至什么操作系统。虽然这对我们来说是好事，但对微软来说可能不是好事。也许他们认为他们的大部分收入来自企业，并认为这种策略会阻止企业开发者采用开放操作系统？我们也不确定它对 Linux 有多好，因为它削弱了它的一大优势——为严肃用户和开发者提供了广泛的工具。

为了避免学究式的评论，我们知道 Linux 是内核，操作系统是内核加上来自 GNU 和其他人的工具。但是通俗点说，人们说 Linux，我们也这么说。虽然 Linux 是“免费”的——如果你支持它并且你的时间有任何价值，那也不完全正确。你可以付钱给像 Red Hat 这样的人来获得你的支持，但是拥有微软的支持是 Windows 的卖点之一。

如果你没有运行 Windows 10，想要无痛的 X Windows，或者只是不想使用微软的工具，总有基于 Cygwin 的 [Swan](https://hackaday.com/2017/03/29/swan-better-linux-on-windows/) 。至于我？我的主要操作系统是 Emacs。[不要告诉艾略特](https://hackaday.com/2016/08/08/editor-wars-the-revenge-of-vim/)。