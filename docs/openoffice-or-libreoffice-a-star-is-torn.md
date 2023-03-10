# OpenOffice 还是 LibreOffice？一颗星星被撕裂了

> 原文：<https://hackaday.com/2020/11/02/openoffice-or-libreoffice-a-star-is-torn/>

说到开源办公套件，大多数人会选择 OpenOffice 或 LibreOffice，它们看起来都非常相似。这并不奇怪，因为它们都是从完全相同的代码库开始的。然而，LibreOffice 团队最近写了一封公开信给 Apache 项目——open office 的当前管理者——要求他们将新用户重定向到 LibreOffice 项目的[。他们的逻辑是 OpenOffice 拥有巨大的知名度，但几年来一直没有新的主要版本。另一方面，LibreOffice 是一个非常活跃的项目。不管怎样，我们都可以为这个案子辩护，但我们不会。但它确实让我们思考事情是如何发展到这一步的。](https://www.libreoffice.org/)

这一切都始于 1985 年德国人 Marco Bö rries 为 Zilog Z80 编写 StarWriter。到 1986 年，他创建了一家公司 Star Division，将文字处理器移植到 CP/M 和 MSDOS 等平台上。最终，该公司增加了其他办公套件程序，由于支持 DOS、OS/2 和 Windows，该套件被称为 StarOffice。

该程序比大多数竞争对手便宜得多，大约花费 70 美元，然而在 1999 年，这个价格点促使太阳微系统公司收购了 StarOffice。我们不是说他们买了一个拷贝或者一个许可证，他们买了整个东西，价格不到 7400 万美元。故事是这样的，它仍然比为每个 Sun 员工购买一个许可证要便宜，特别是因为大多数人同时拥有一台 Windows 机器和一台 Unix 机器，这仍然需要一些功能。

## 孙负责

Sun 在 2000 年提供了 StarOffice 5.2 作为个人使用的免费下载，这使得该软件受到了很多关注。它最终在开源许可下发布了大部分代码，产生了 OpenOffice。Sun 为这个项目做出了贡献，并定期对代码进行快照，以推广 StarOffice 的未来版本。

这是一段时间的事态。StarOffice 6.0 对应的是 OpenOffice 1.0。2003 年，1.1 版变成了 StarOffice 7。几年后，StarOffice 8/OpenOffice 2.0 出现了，到 2008 年，我们有了 StarOffice 9 和 OpenOffice 3.0，就在甲骨文进入市场之前。

## 然后甲骨文出现了

2010 年，甲骨文收购了 Sun。所有的一切。对于他们购买的一些东西，他们似乎没有太多的计划，StarOffice 就是其中之一。他们把这个程序重新命名为 Oracle Open Office。他们还在许可方面做了一些奇怪的事情。例如，StarOffice 9 不再对教育客户免费，但他们可以使用 StarOffice 8，当然，也可以坚持使用 OpenOffice，放弃支持。

2011 年，甲骨文决定取消商业服务，留下 OpenOffice，这是 StarOffice flame 的官方社区守护者。他们把责任交给了 Apache 软件基金会。

不过，很明显，StarOffice 5.1 仍将在 Windows 10 上运行，正如[RickMakes]在下面的视频中演示的那样:

 [https://www.youtube.com/embed/HzKD4qQSJBo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/HzKD4qQSJBo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



## 开源与图书馆的崛起

当然，一旦代码在 2000 年左右开源，人们就可以自由地创建衍生项目，他们也确实这样做了。虽然已经有几个著名的分支，包括 NeoOffice 和 Go-oo，但只有 LibreOffice 真正强大，即使 NeoOffice 和最初的 OpenOffice 仍然活跃。但是，NeoOffice 只针对 Mac。时间线有点让人摸不着头脑，但维基百科有一个很棒的图表展示了它:

[![](img/7d957c8823483c1b75e7f0e1490dd3b1.png)](https://hackaday.com/wp-content/uploads/2020/10/star.png)

当 Oracle 出现时，大多数 OpenOffice 开发人员组成了 LibreOffice。从那以后，LibreOffice 一直处于非常活跃的开发阶段，现在大多数 Linux 发行版都将其作为默认的办公套件。根据 LibreOffice 的信，他们在 2019 年有 15，000 次代码提交，而同期 OpenOffice 有 595 次。他们已经发布了 13 个主要版本，而 OpenOffice 已经六年没有一个主要版本了。

## 许可证特性

我们不是开源律师——也不是任何类型的律师，但其中一个问题源于这两个项目如何获得许可。OpenOffice 使用 Apache 许可证，而 LibreOffice 使用双 LGPLv3/Mozilla 公共许可证。

由于一些法律原因，OpenOffice 做的任何事情都可以被整合到 LibreOffice 中，许可条款允许这样做。但是如果 LibreOffice 添加了什么东西，比如字体嵌入，OpenOffice 就不能合法地合并那个代码。如果你想知道细节，你可以阅读来自自由软件基金会的这篇文章。IBM 提供了一些来自 Lotus Symphony 的代码，这些代码可能没有正确地放入开源领域，这使得问题变得更加复杂。

## 回到信里

这是一次旅程，但是本月早些时候 LibreOffice 发给 Apache 项目的公开信又如何呢？我们可以争论这封信的任何一方。一方面，生活在开源世界的一部分是理解其他人能够并且愿意开发并行项目。然而，我们可以理解一些人去 OpenOffice 并认为那里没有什么新东西的沮丧。当然，也有其他开源套件，但是考虑到这两个项目的兄弟关系，我们可以理解他们的观点。但是用户可能会很乐意使用 Calligra(以前是 KOffice)或者 OnlyOffice，这两个都是开源的。

你怎么想呢?OpenOffice 应该认输吗？开始评论。