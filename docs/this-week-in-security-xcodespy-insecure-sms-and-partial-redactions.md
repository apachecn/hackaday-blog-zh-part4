# 本周安全:XcodeSpy，不安全短信，和部分修订

> 原文：<https://hackaday.com/2021/03/26/this-week-in-security-xcodespy-insecure-sms-and-partial-redactions/>

恶意软件似乎有了新的趋势，目标是开发人员及其开发和构建流程。吸引力是显而易见的:攻击者只需要感染开发机器，而不是努力构建和销售恶意应用程序。倒霉的被感染的开发人员现在可以努力传播恶意负载了。

最新的例子是由一名不愿透露姓名的研究人员发现的 [XcodeSpy](https://labs.sentinelone.com/new-macos-malware-xcodespy-targets-xcode-developers-with-eggshell-backdoor/) 。它的工作原理是使用 Xcode IDE 的`Run Script`函数来运行一个脚本，这个脚本会完全打开你的电脑的后门。该实例是在一个重新包装的开源项目 TabBarInteraction 中发现的，但他们只是无辜的受害者。对于某些人来说，在构建过程中插入一个脚本，并分发新的、掺杂的包是非常简单的。这可能不是唯一的一个，所以请注意`Run Scripts`的模糊负载。

## Drupal 模块安全性

Drupal 很像 WordPress，因为核心项目很少有严重的漏洞，但是在可用扩展库中经常会发现非常严重的问题。举例来说，[快速自动完成模块有一个“中等严重”的漏洞](https://www.drupal.org/sa-contrib-2021-005)。这里有两个有趣的点。首先是问题本身，这是一个数据暴露问题。这个扩展提供了一个搜索栏体验，显示建议的自动完成，并提供与该自动完成相关的片段。默认情况下，这些搜索结果仅限于匿名用户在网站上可以访问的内容。该扩展还提供了搜索私人内容的选项，使用访问站点的用户可用的权限。问题是扩展缓存了所有这些结果，并且没有在缓存中正确地分离结果。因此，一旦特权用户搜索了某个隐私内容，任何用户都可以重复搜索并访问片段，即使该信息位于不可访问的页面上。

Drupal 做了一些有趣的事情，叫做他们的[安全顾问政策](https://www.drupal.org/drupal-security-team/security-advisory-process-and-permissions-policy)。简而言之，Drupal 团队选择了一些广泛使用的扩展，并为这些项目提供有限的安全支持。这似乎主要意味着协调漏洞公告。

## 细胞数量危险

你知道几乎每个在线服务商都想知道你的手机号码吗？其中一个原因是，接收短信是最受欢迎的第二认证因素之一，更不用说帐户恢复机制了。虽然这很受欢迎，但这是一个可怕的想法。有多种针对 SMS 的攻击，通过这种恢复过程很容易导致帐户被接管。攻击者可以打电话给你的移动服务提供商，为你的号码申请一张新的 SIM 卡，这就是所谓的 SIM 交换攻击。他们可以欺骗你的身份到 SS7 网络，导致短信和语音通话间谍。不要忘记日益流行的号码迁移欺诈，攻击者声称是你，将你的号码转移到新的提供商。

事实证明，有一种更简单的方法来拦截短信。[Lucky225]多年来一直对短信诈骗感兴趣，[为我们带来了他在短信路由](https://lucky225.medium.com/its-time-to-stop-using-sms-for-anything-203c41361c80)方面的工作。NetNumber ID 是一种路由服务，旨在供 VoIP 和商业用户处理文本消息，即使他们没有使用传统的 SMS 设备。这一过程明显缺乏监管，直到最近，通过一个简单的请求就可以劫持任何手机号码的短信路由。 [Vice 有一个很好的例子](https://www.vice.com/en/article/y3g8wb/hacker-got-my-texts-16-dollars-sakari-netnumber)[lucky 225]演示了这次攻击，用了 16 美元和一封假的授权书。

## 缩放显示太多

在 Zoom 上过度分享是我们对 2020 年的一种有趣的、令人不快的、有时令人不安的集体记忆。从室友走进镜头，到不穿裤子开会，那是一段疯狂的时光。还有另一种过度共享的方式，至少在你共享桌面或打开的应用程序的视频时是这样。当你共享桌面视图时，不要在你的机器上打开任何敏感的东西，这是常识。然而，来自 SySS 的两名研究人员发现，即使只共享一个应用程序，[其他应用程序窗口也可能会短暂出现在视频提要](https://www.syss.de/fileadmin/dokumente/Publikationen/Advisories/SYSS-2020-044.txt)中。

当一个不同的应用程序被绘制在通过缩放捕获的应用程序之上时，发送的视频的几帧可能包含该应用程序的图像。如果通话被另一方录了下来，他们可以拉下画面，看到的正是无意中看到的。现在，这通常就像查看打开的浏览器标签，或者查看通话记录一样平常。从密码管理器到个人信息，这个 bug 肯定会以非常糟糕的方式结束。

 [https://www.youtube.com/embed/SonmmgQlLzg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/SonmmgQlLzg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



## 部分~~修订~~

![Mostly Redacted RSA Key](img/c43f56e285ddc999867cdfc781293b11.png)说到无意的数据泄露，我遇到了一个有趣的故事，关于[一个被部分编辑的 RSA 密钥，它被发布在网上](https://blog.cryptohack.org/twitter-secrets)。正如我们很多人习惯做的那样，一些密码极客开始试图从部分截图中找出整个密钥。不到三个小时，他们就推断出了完整的密钥。文章指出，最困难和最耗时的部分是将截图转换回文本。

多年来，有许多关于修订失败的故事。有时可以通过简单的复制和粘贴来阅读编辑过的 pdf。在某些图像中，您可以根据被删除文本上下可见的一行像素来识别文本。最后，照片编辑套件中的简单模糊工具是可逆的，可以轻松恢复文本。综上所述，正确地进行编辑是非常困难的，正如文章总结的那样，“如果你发现了一些隐私，就保持这样。”