# 谁在考虑开源固件？

> 原文：<https://hackaday.com/2022/05/14/who-is-thinking-about-open-source-firmware/>

昨天，我们发表了一篇关于 NVIDIA 宣布为其最新的显卡开发开源驱动程序的文章。Hackaday 是*开源软件和硬件的巨大支持者，你会认为我们在倒香槟。但事情比这更棘手。*

他们能够发布全新的开源驱动程序的部分原因是，他们希望保留的秘密已经转移到了固件*中。那么，整个系统是更开放还是更开放呢？是啊，也许两者都有。*

 *随着硬件和操作系统之间更加开放的接口，人们将驱动程序移植到不同架构的工作将变得更加容易。现在驱动程序层中的错误应该可以更快地被发现和修复。所有常见的开源论点都适用。但与此同时，整个系统并没有变得更加透明。关于新的 NVIDIA 驱动程序的讽刺之处在于，几十年来我们一直在推动它们变得更加开放，而它们的回应是将其秘密写入固件。

从软件转移到固件的秘密仍然是秘密，甚至我们当中最坚定的开源支持者也已经关闭了我们计算机中的硬件和固件路径。以[英特尔管理引擎](https://hackaday.com/2017/12/11/what-you-need-to-know-about-the-intel-management-engine/)为例，它是您电脑中的一台小型电脑，一直在运行，甚至在电脑“关闭”时也是如此。你想审计代码吗？抱歉。这并不像它没有公平的份额[安全相关的错误](https://hackaday.com/2017/12/07/another-defeat-of-the-intel-management-engine/)。

当然，兔子洞会更深。没有现代的 X86 芯片真正运行 X86 机器语言指令——相反，它们有一个微码解释器来读取机器语言并将其解释为芯片真正所说的内容。这非常方便，因为这意味着芯片供应商可以通过简单地推出固件更新来解决硅缺陷。但这也意味着你的 CPU 在内核运行一个秘密的固件层。这一层当然[不是没有 bug](https://hackaday.com/2021/03/26/undocumented-x86-instructions-allow-microcode-access/)，其中一些可能有安全相关的暗示。

这对于你的智能手机来说更是如此，因为你的智能手机中充斥着多个处理器，它们或多或少地协同工作来完成任务。因此，虽然 Android 用户生活在比他们的 iOS 兄弟更开放的环境中，但当你开始向下看固件层时，一切都是一样的。操作系统的顶层*是*开放的，但它正漂浮在二进制斑点的海洋之上。

这些与你有多大关系可能取决于你打算用这个设备做什么。如果你对开源感兴趣是因为你喜欢破解软件，那么拥有开放驱动是一个极好的资源。如果你期待开放性提供的安全保证，那么，你很不幸，因为你仍然不得不盲目地信任固件。如果你对开源感兴趣，因为漏洞往往会被更快地发现，这是一种混合——虽然顶级驱动程序变得更容易检查，但代码的其他部分却被推向更深的晦涩。也许是时候开始关注开源固件了？

This article is part of the Hackaday.com newsletter, delivered every seven days for each of the last 200+ weeks. It also includes our favorite articles from the last seven days that you can see on [the web version of the newsletter](https://mailchi.mp/hackaday.com/hackaday-newsletter-649368). Want this type of article to hit your inbox every Friday morning? [You should sign up](http://eepurl.com/gTMxQf)!*