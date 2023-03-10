# 文书工作完成之前还没结束:试驾 TiddlyWiki

> 原文：<https://hackaday.com/2020/02/14/it-aint-over-til-the-paperwork-is-done-test-driving-tiddlywiki/>

做项目很有趣。记录它们通常没有那么多。然而，如果你想让任何人重复你的工作——或者只是想记住几年前你在做什么，什么东西需要升级或修理。

有很多方法可以记录你项目的细节。我们喜欢看到事情是如何走到一起的，当然我们也很乐意建议在 [Hackaday.io](http://hackaday.io) 上进行记录。但有时，你只想把自己的笔记留给自己。当然，笔记本总是有的，但这似乎有点过时了。很多项目都在维基上，但是你讨厌仅仅为了做笔记而建立一个网络服务器和一个维基实例。但是，如果你可以用最少的设置拥有一个本地维基呢？

我最近偶然发现了 TiddlyWiki ，并决定带它去兜风。休息后和我一起去看看到底是怎么回事。

## 低开销维基

使用 TiddlyWiki，您可以在一个文件中存储一个非常好的 Wiki。如果你不喜欢依赖互联网连接，你可以把它存储在你自己的电脑或闪存盘上。但是如果你愿意，你也可以把它放在云上。你甚至可以把它保存到 Hackaday.io，尽管你必须压缩它，因为这个平台不接受直接的 HTML 文件。

单个文件可以获得多少功率？其实还挺多的。基础设施是一个单一的 HTML 文件，所以也许你不能用它来托管维基百科。但是你可以修改 HTML 文件，事实上，有很多插件和其他东西你可以添加，即使你的 HTML 技能还不足以自己完成。但稍后会详细介绍。

## 基础

[![](img/a667a7b6e1f95c8606d059fbc26727a7.png)](https://hackaday.com/wp-content/uploads/2020/01/wiki0.png) 入门太容易了，tust [下载一个空的 TiddlyWiki 模板](https://tiddlywiki.com/)。你可以给它起任何你喜欢的名字，当你用网络浏览器打开它的时候，你会看到它给你一个设置的表格。这个表单实际上是写在维基上的，所以这应该会让你知道它有多强大。

该文件将包含一个或多个主题，称为小标题。这些可以是可见的或隐藏的，有许多方法可以找到，打开和关闭它们。每个 tiddler 都可以有标签和超链接。例如，您可以构建一个侧边栏，列出所有标有菜单标签的小标题。或者你可能想用那个标签来标记你所有的 RISC-V 小程序，这样你就可以很容易地找到它们。您还可以在另一个 tiddler 中搜索或动态包含一个 tiddler。

每次你打开一个小工具，它都会增加你的视野。你可以关闭任何你不想要的。如果你想专注于你的工作，你也可以最小化它们或者你可以最小化或者关闭所有其他的小程序。

## 保存和其他功能

唯一的小问题是你如何保存你的改变？在默认的在线 Wiki 中，有一个名为“ [GettingStarted](https://tiddlywiki.com/#GettingStarted) 的主题，它实际上向您显示了您根据平台和网络浏览器细分的所有选择。有一些连接器可以将你的文件存储在本地或各种云服务上，包括 GitHub。还提供了浏览器扩展，使得使用 TiddlyWiki 更加容易。不是只有一种方式，每个人的情况都会不一样。最坏的情况是，你可以选择下载更新的 Wiki，就像你在浏览器中下载任何其他文件一样。

[![](img/48bce95dc47bb5c9ea822f33a9ba6f2e.png)](https://hackaday.com/wp-content/uploads/2020/01/savers.png) 你可以用一个小程序来存储书签、组织任务、保存清单、组织图片——你甚至可以编辑图片。好的一面是，因为它都在一个文件中，你可以很容易地把它发送给别人，他们只需一个网络浏览器就可以打开它。事实上，你可以把它发布到网上，作为一个网站使用——tiddlywiki.com 网站就是这么做的。

## 插件

有各种各样的插件可以安装。比如有一个语法着色插件。另一个将把 Twitter 数据嵌入维基。除了标准插件，还有许多用户贡献的插件。例如，您可以获得从 Evernote 迁移、生成二维码或与 Google Analytics 合作的工具。

特别令人感兴趣的是一个提供 CodeMirror 编辑器的插件。它是用来编辑代码的，你可以为它安装额外的特性，比如语法高亮、括号完成和键映射。

除了插件，你还可以下载更多的主题和语言。有些主题是装饰性的，但有些是实用性的。例如，您可以安装一个隐藏编辑 tiddler 功能的主题。如果你用它来发布一个网站，这将是非常有用的。您也可以要求输入密码才能保存。

还有很多宏和小部件。例如，有一个名为 [< $codeblock >](https://tiddlywiki.com/static/CodeBlockWidget.html) 的小部件，它会适当地显示一段代码。甚至还有一个加密部件。宏允许您为想要在小程序中重复的内容定义快捷方式，或者如果您将它放在正确的位置，为多个甚至所有小程序定义快捷方式。也可以用 Javascript 编写宏。

## 独立地

这并不是一个完整的 TiddlyWiki 教程——网上有很多。如果你更喜欢视频，下面的系列也将帮助你开始。

 [https://www.youtube.com/embed/ZMGpAW0z_Bo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent&listType=playlist&list=PLzZCajspPU_UjFn0uy-J9URz0LP4zhxRK](https://www.youtube.com/embed/ZMGpAW0z_Bo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent&listType=playlist&list=PLzZCajspPU_UjFn0uy-J9URz0LP4zhxRK)



你可以用 TiddlyWiki 做任何事情。我们甚至看到它被用来构建一个冒险游戏。如果您现在正在使用它，或者您打算使用它，请留言告诉我们如何使用。我们已经看到 wikis 被用于许多简洁的文档，包括[信号识别](https://hackaday.com/2015/09/11/strange-signals-sigidwiki/)。因为这个系统很容易扩展，我们想知道你是否可以把一个 [Jupyter 笔记本](https://hackaday.com/2019/02/22/drops-of-jupyter-notebooks-how-to-keep-notes-in-the-information-age/)放进去？