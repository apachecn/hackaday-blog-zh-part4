# 看代码:宽屏咆哮

> 原文：<https://hackaday.com/2020/06/20/seeing-code-the-widescreen-rant/>

几周前，Linus Torvalds [制定了法律](https://lkml.org/lkml/2020/5/29/1038)，以一种特别 Linus 的方式。在一个软件社区中，制表符和空格可以引发宗教战争，说 80 个字符宽的代码已经过时，对一些人来说，完全是异端邪说。关于我们如何来到这里的更多背景，请阅读[斯文·格雷戈里]在 hack aday 上的[历史文章，你会了解到切片面包和 80 个字符的 IBM 打孔卡都是在 1928 年 7 月首次亮相的。但是我跑题了。](https://hackaday.com/2020/06/18/ask-hackaday-are-80-characters-per-line-still-reasonable-in-2020)

当我看一个代码库的时候，我喜欢看它的*结构*，我不是一个人。这就是 [Linux 内核风格指南的](https://www.kernel.org/doc/html/v4.10/process/coding-style.html)宽得离谱的 8 字符标签的原因之一。结合变量名变得越来越具有描述性的趋势(我认为这是一件好事),以及显示器的长宽比似乎永无止境的增长(我不这么认为), 80 列的宽度似乎是 VT-220 时代的遗物。

[![Hazeltine Terminal](img/79770577cdbf1f5ac443abca1440d4ae.png)](https://commons.wikimedia.org/wiki/File:%D0%A2%D0%B5%D1%80%D0%BC%D0%B8%D0%BD%D0%B0%D0%BB_Hazeltine_1500.jpg "Sh ipa / CC BY-SA (https://creativecommons.org/licenses/by-sa/4.0)") 在莱纳斯的信中，我们了解到他运行 100 x 50 的终端，并经常将它们拖到 142 x 76 的屏幕上。(业余！我现在以 187 x 48 的分辨率给你写下这些。)当你运行这么宽时，换行参数列表没有任何意义，即使你使用匈牙利符号。

然而，改变是痛苦的。我不得不重新格式化代码以满足一本书 73 列的限制，却发现我的行内注释太冗长了。即使取消像 80 列限制这样的人为限制，也会产生真正的效果。例如，我在更宽的屏幕上写更长的段落。

不过，我看到了一些好的方面。如果单一的思想可以用单行来表达，它使得代码的形状更好地反映了它的功能。摆脱无意义的环绕占据更少的垂直空间，这在今天的电影监视器上是非常珍贵的。而如果让行内评论更好(我知道，又是一场圣战！)或促进更好的变量命名，这将是值得的。

但是无论你如何看待它，我们都不再是在敲旧的 80 个字符的哈泽泰。是时候让我们的编码风格和实践跟上了。

This article is part of the Hackaday.com newsletter, delivered every seven days for each of the last 200+ weeks. It also includes our favorite articles from the last seven days that you can see on [the web version of the newsletter](https://mailchi.mp/hackaday.com/hackaday-newsletter-649368). Want this type of article to hit your inbox every Friday morning? [You should sign up](http://eepurl.com/gTMxQf)!