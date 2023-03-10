# 本周安全:上升气流，特穆克斯和 Magento

> 原文：<https://hackaday.com/2022/02/25/this-week-in-security-updraft-termux-and-magento/>

最受欢迎的 WordPress 备份插件之一 UpdraftPlus，[发布了一组更新 x.22.3](https://updraftplus.com/updraftplus-security-release-1-22-3-2-22-3/) ，其中包含对 CVE-2022-23303 的潜在重要修复。该漏洞会将现有备份暴露给任何登录的 WordPress 用户。这个 bug 是由 Jetpack[的人发现的，他们对此有很好的报道](https://jetpack.com/2022/02/17/severe-vulnerability-fixed-in-updraftplus-1-22-3/)。这是一个常见问题实例的组合，即缺乏正确身份认证的终端。heartbeat 函数允许任何用户访问它，并返回最新的备份 nonce。

加密随机数是一个不完全是加密秘密的值，但只使用一次。在某些情况下，这是为了减轻重放攻击，或者用作初始化向量。在 UpdraftPlus 的情况下，nonce 充当单个备份的唯一标识符。数据泄漏可以与`maybe_download_backup_from_email()`函数中的另一个弱验证相结合，以允许下载备份。由于 WordPress 备份将包含敏感信息，这是一个相当大的问题。目前还没有这种攻击被使用的已知实例，但是一如既往，现在就更新以保持领先。

## 泰尔穆克

发现我们中的许多人在 Android 上使用 Termux 应用程序并不奇怪。这几乎相当于为命令行工具安装一个真正的 Linux 发行版，甚至运行一些图形化的 Linux 应用程序。你可能不知道的是，谷歌 Play 商店上的版本已经远远过时了，因为 Android 10 中的 Android 安全政策发生了变化。这只是很烦人，但现在这是一个真正的问题，因为[Termux 应用程序中已经公布了一系列漏洞](https://termux.org/general/2022/02/15/termux-apps-vulnerability-disclosures.html)。两个最严重的问题分别需要`Termux:Tasker`和`Termux:Widget`附件。Tasker 没有定义允许通过意图执行的权限，所以任何其他应用程序都可以触发命令。除此之外，还有一个简单的目录遍历攻击，因此该命令可以引用任何二进制 Termux 可以访问的内容。

小部件的问题也类似，但是这个应用程序至少有一个 auth token，它被检查输入意图。问题是，有了有效的令牌，任何命令都可以运行。最重要的是，第三个漏洞是文件权限问题，任何应用程序都可以读取 Termux 文件，包括颁发的令牌。在考虑这个 bug 的严重性时，还有一个问题需要考虑，那就是根源手机。如果您正在运行一个`su`二进制文件，并且您已经给了 Termux root 权限，那么上述漏洞会突然严重得多。

## Magento 和 Adobe 商务

在 Magento 项目中，甚至在 Adobe Commerce 中，都有一个非常严重的漏洞。 [CVE-2022-24086 于 2 月 13 日](https://helpx.adobe.com/security/products/magento/apsb22-12.html)宣布成为无需认证即可访问的 RCE。更糟糕的是，它似乎很容易被利用，尽管精确的概念验证还没有公开。Adobe 修补了这个漏洞，几天之内，[的研究人员绕过了他们的修补程序](https://threatpost.com/new-critical-rce-bug-found-in-adobe-commerce-magento/178554/)，导致 CVE-2022-24087 被发布。Sansec 的研究人员已经在 T4 看到了野生环境中的攻击。现在打补丁，给任何 Magento 安装一个潜在的恶意软件非常密切的外观。

> Magento 2 发布了一个新的修补程序，以减轻预认证的远程代码执行。如果您用第一个补丁打了补丁，这不足以保证安全。
> 请再次更新！[https://t.co/vtYj9Ic6ds](https://t.co/vtYj9Ic6ds)@ ptswarm(因为你也有过 PoC！) [#magento](https://twitter.com/hashtag/magento?src=hash&ref_src=twsrc%5Etfw)
> 
> —布莱克利斯(@布莱克利斯 _)[2022 年 2 月 17 日](https://twitter.com/Blaklis_/status/1494363202074914822?ref_src=twsrc%5Etfw)