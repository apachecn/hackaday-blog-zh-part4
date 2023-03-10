# 在 Emacs 上经营的面包店

> 原文：<https://hackaday.com/2019/03/06/the-bakery-that-runs-on-emacs/>

说到在专业面包店管理配料和烘焙，我们知道大多数人会求助于 SQL 数据库和 emacs。真的，你还需要什么？好吧，也许有些人会认为 emacs 在这方面帮不了你，所以，这里是[Piers]如何使用 [emacs 和 PostgresSQL 来管理他的面包店](https://bofh.org.uk/2019/02/25/baking-with-emacs/)的日常需求。

[Piers]曾尝试用电子表格来记录事情，但当他不得不创建一个新配方时，他并不真正喜欢它:“大量繁琐的复制、粘贴和重复公式”，他是这样说的。作为一名前职业程序员，[Piers]对 emacs 很熟悉，因此使用 org-mode 在 emacs 中建立了一个每日工作表。每天早上，他运行 org-capture 来创建当天工作的模板。org 文件中的一些代码(用 org-babel 运行)可以在数据库上运行查询。他创建了一些代码来设置每天的日志条目，并运行他需要的复杂的数据库查询。

(Piers)接下来要做的事情有一个清单，包括配料订单管理和会计，但这对他很有用。为了阻止任何可能爆发的潜在战争，最好提一下这个系统就是这么做的:它为他工作。还有其他的可能性。看看 Al 的[编辑战](https://hackaday.com/2016/07/26/editor-wars/)的文章，或者 Elliot 的[反驳](https://hackaday.com/2016/08/08/editor-wars-the-revenge-of-vim/)，或者，忽略战争，阅读这篇关于[用蒸汽烘焙](https://hackaday.com/2012/06/27/baking-better-bread-with-steam/)的文章。