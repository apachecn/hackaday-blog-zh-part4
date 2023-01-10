# 复制和粘贴被认为不安全

> 原文：<https://hackaday.com/2020/06/18/copy-and-paste-deemed-insecure/>

早在 Windows NT 称王的时候，微软就可以宣称它满足了 C2 严格的“黄皮书”安全认证。有什么问题吗？不要安装网络和移除软驱。事实证明，你想用电脑做的大部分事情都是有安全风险的。甚至[复制粘贴](https://research.securitum.com/the-curious-case-of-copy-paste/)。

[Michal Benkowki]对他的研究有一个很好的总结，可以归结为以下攻击场景:

1.  访问恶意网站。
2.  复制一些东西到剪贴板，这使得网站可以放入一个危险的有效载荷。
3.  使用基于浏览器的可视化编辑器(如 Gmail 或 WordPress)访问另一个网站
4.  将剪贴板粘贴到编辑器中。

问题是编辑器接受 HTML 数据，这允许剪贴板插入 JavaScript。如果您从未在 API 级别使用过剪贴板，那么您可能会惊讶地发现，剪贴板通常一次包含多个项目。例如，剪贴板可以同时包含一些纯文本、一些 HTML 和一种特殊的专有格式。不过，据推测，所有这些项目都代表相同的信息。

浏览器意识到了这个问题，并试图清除它们放在剪贴板上的文本。[Michal]将“[复制并粘贴操场](https://cdn.sekurak.pl/copy-paste/playground.html)”放在一起，以允许探索和演示浏览器会接受和不会接受什么。

这篇文章的其余部分涵盖了几个主要浏览器和编辑器系统中的修复错误，包括 GMail 和 Google Docs。也有一些关于一些系统的讨论，这些系统还没有被命名，因为错误还没有被修复。

[Michal]非常彻底，不出所料，他为自己的工作获得了大约 3 万美元的奖金。我们已经习惯了在[物联网设备](https://hackaday.com/2017/03/22/shut-the-backdoor-more-iot-cybersecurity/)上看到漏洞，但有点令人惊讶的是，像剪贴板这样普通的东西也能构成威胁。如果你想自己申请一些 bug 奖励，也许明年你可以试试[黑一颗卫星](https://hackaday.com/2020/04/30/the-unites-states-air-force-would-like-you-to-hack-into-their-satellite/)。