# 问 hack aday:Windows XP 源代码泄露是坏事吗？

> 原文：<https://hackaday.com/2020/09/25/ask-hackaday-is-windows-xp-source-code-leak-a-bad-thing/>

一夜之间，Windows XP 源代码被泄露的消息传来。The Verge 称他们已经“验证了这些材料是合法的”,泄露的内容还包括 Windows Server 2003 和一些 DOS 和 CE 代码。问题是，自从微软放弃对 XP 的支持以来，现在已经[六年多了，源代码公开真的有关系吗？](https://www.microsoft.com/en-us/microsoft-365/windows/end-of-windows-xp-support)

## 毒丸

正如 Erin Pinheiro 在[她今年早些时候关于任天堂知识产权泄露的优秀文章](https://hackaday.com/2020/05/21/no-the-nintendo-leak-wont-help-emulator-developers-and-heres-why/)中所指出的(顺便说一句，这可能是今年 Joe Kim 的最佳作品)，合法的开发者不能真正利用泄露的代码，因为这将他们暴露在潜在的诉讼面前。微软有一个强大的法律机器，肯定会追查像这样的代码泄漏滥用。Erin 在她的文章中提到，仅仅看代码对竞争对手来说是危险的。

即使其他软件公司确实查看了源代码并实现了他们自己的改进而没有越过法律界限，又有多少收益呢？当然，有这种动机的公司现在应该已经逆向设计了早已过时的操作系统的秘方，对吗？

## 间谍大战间谍

接下来想到的是安全问题。在撰写本文时， [statcount 估计 Windows XP 的市场份额为 0.82%](https://gs.statcounter.com/os-version-market-share/windows/desktop/worldwide/)，这仍然是一个非常大的数量。也许一个更好的问题是，哪些*类型的*机器仍在运行它？我没有找到任何硬数据来回答这个问题，但是有像核磁共振这样的专用机器没有简单的升级途径，仍然使用操作系统，还有[嵌入式版本的 XP](https://en.wikipedia.org/wiki/Windows_XP_editions#Windows_XP_Embedded) ，运行在销售点、自动柜员机、机顶盒和其他长期硬件上，这些硬件因其所有者不升级而臭名昭著。

无论从怀特哈特还是布莱克哈特的角度来看，源代码都是追踪漏洞的福音。破解系统或提交漏洞修复程序会有更多收获吗？操作系统已经寿终正寝，然而微软已经表明，足够大的安全威胁仍然需要一个补丁，就像他们在 2019 年 5 月对[远程桌面协议漏洞补丁所做的那样。我想知道这些代码是否仍在 Windows 10 中使用，因为这将使它成为安全研究人员的一个有趣工具。](https://hackaday.com/2019/05/21/this-week-in-security-whats-up-with-whatsapp-windows-xp-patches-and-cisco-is-attacked-by-the-thrangrycat/)

至于泄露的危险信息，已经发现了一些私钥，像[NetMeeting 根证书](https://twitter.com/gsuberland/status/1309366364537266177)。但是很难说像这样的密钥有多大的风险是由于软件的年龄。你应该停止使用 NetMeeting 进行高安全性的视频会议，如果你还没有这样做的话…13 年前[就寿终正寝了](https://www.pcworld.com/article/113659/article.html)，所以这没什么好奇怪的。

## 你可能会学到一些东西

我认为像这样的代码泄漏最大的新闻是从中学习的能力。为什么人们会看开源项目的源代码？当然，你可能正在修复一个 bug 或者添加一个特性，但是很多时候是为了看看其他程序员是如何做事情的。这是数字时代的学徒计划，拥有早已死亡的项目的源代码既保留了事情是如何完成的，以供以后研究，又让未来好奇的超级明星在大师的肩膀上磨练他们的技能。

## 就像一个证明艺术品合法性的博物馆

为什么公司不走在前面，将生命周期结束的代码作为开源代码发布呢？这将保证代码的有效性。就目前的情况而言，如何验证从互联网上光线更暗的角落获取的泄漏代码？发布生命周期结束项目的官方源代码保存了历史，这是互联网时代从未考虑过的事情，但我们应该这样做。我们已经[听到该公司宣传微软热爱开源的信息](https://pulse.microsoft.com/nl-nl/business-leadership-nl-nl/na/fa1-microsoft-loves-open-source/)，这是另一个通过发布源代码来表明这一点的好机会，因为它已经从这次泄露中出来了。现在这样做将是一个很大的进步，而且在未来生命周期结束的产品发生泄漏之前采取更好的措施。

这是一个不切实际的想法，当我们遇到[物联网公司倒闭并在倒闭时出售其硬件](https://hackaday.com/2020/02/29/the-iot-trap/)的故事时，我们经常会提出这个想法。在这种情况下，源代码将允许用户推出他们自己的不再存在的后端服务，但微软可能会反对基于他们自己代码的“LibreWinXP”项目。很可能该公司仍然有一些长期合同为使用 XP 硬件的实体提供支持。

## 你觉得怎么样？

这是*问黑客日*，所以我们想知道你对此的看法。旧源代码泄露，是坏事吗？有什么令人信服的理由让那些已经寿终正寝的项目的源代码成为秘密吗？现在 XP 代码就在某个地方，你认为它会带来什么？在下面称重！