# 大量的 Linux 工具

> 原文：<https://hackaday.com/2021/06/21/a-collection-of-linux-tools-on-steroids/>

有时候我们做事情是因为“我们一直都是这样做的。”例如，螺钉在 16 世纪有开槽头，开槽头是出了名的糟糕，但尽管罗伯逊在 1907 年和菲利普斯在 20 世纪 30 年代，开槽螺钉头花了几十年才变得不常见，它们仍然潜伏在一些地区。我们每天使用的许多 Linux 工具都是已经存在了近半个世纪的 Unix 工具的直接后代。我们之前已经看过一些更现代的替代工具，而且[ibraheemdev]有一个由许多这样的工具组成的 [GitHub 集合](https://github.com/ibraheemdev/modern-unix)，值得一试。

当然，现代并不总是意味着更好。然而，列表中的工具确实有很棒的特性，包括过去不常见的东西，比如颜色的使用、基于文本的图形以及 git 集成等。

一些命令取代了非常常见的命令。比如，`bat`就像是`cat`，有语法着色和 git 集成。`exa`和`lsd`命令就像`ls`，`lsd`甚至可以兼容`ls`。有`delta`代替`diff`，有`duf`或`dust`代替`du`。代替`cd`，你可以使用`zoxide`来获得一些本地的高级功能，所以一些 shells。

许多命令提供较少的功能来简化常见任务。例如，您可以使用`sed`来搜索和替换文本，但`sd`更容易。你可以使用`cut`来提取文件的一部分或者流出来，但是`choose`让它变得更容易。有时`man`命令会给你太多详细的信息。`tldr`和`tealdeer`命令只给你命令的通用选项，而`cheat`提供交互式备忘单。

列表中的其他命令提供了专门的网络帮助，您可以使用`telnet`、`wget`或`curl`。例如，`xh`、`curlie`和`httpie`等程序提供了更简单的方式来处理各种网络请求。

您可能不会使用这个列表中的每个命令，手指记忆非常强大(尽管如果您足够勇敢，您总是可以创建一个别名)。但是，您可能会发现一两个有趣的命令已经成为您工作流程的一部分，如果它们还没有成为工作流程的一部分的话。

我们在以前的 Linux Fu 帖子中已经讨论过这些工具中的一些[，但是将这些工具放在一个集合中是很方便的，而且——我们认为——列表会不时更新，所以值得在 GitHub 上观看这个项目。](https://hackaday.com/series_of_posts/linux-fu/)

这不是我们第一次看到像《T2》这样的榜单，尽管每个人似乎都有一些其他人没有的东西。如果你发现自己经常编写难懂的命令行，看看`[Marker](https://hackaday.com/2018/10/24/linux-fu-marker-is-a-command-line-menu/)`，这会有所帮助。

横幅图片:[【企鹅群小】](https://www.flickr.com/photos/56521678@N04/5220534077) 由[南极洲开往](https://www.flickr.com/photos/56521678@N04)。 [CC BY-ND 2.0](https://creativecommons.org/licenses/by-nd/2.0/?ref=ccsearch&atype=rich)