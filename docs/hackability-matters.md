# 黑客能力很重要

> 原文：<https://hackaday.com/2021/01/16/hackability-matters/>

[Unix 的方式](https://en.wikipedia.org/wiki/Unix_philosophy)提供了极端的黑客能力。这个想法是，软件应该被编写为完成离散任务的工具，并且应该是模块化的、可扩展的，并且与其他工具配合良好。这就像是一套乐高玩具软件——你可以在一定范围内随心所欲地将积木组合在一起，做出比任何一个单独的积木都酷得多的东西。

显然，这并不适用于所有的应用程序——像图形编辑器和 web 浏览器这样的东西并不能真正成为与其他应用程序很好集成的优雅工具，对吗？它们是臃肿的围墙花园是很自然的。在浏览器中发生的事情必须留在浏览器中，对吗？

但是，你整天使用的一个软件，你进入网络空间的窗口，却不能与你系统的其他部分很好地配合，这有多可悲？老实说，我从来没有真正被这个事实困扰过，直到偶然发现了 TabFS。这是 Chrome 的一个扩展，它将浏览器上的选项卡表现为本地系统上的文件 Unix Way。这意味着任何其他可以读写文件的程序都可以打开标签、收集标签、动态改变网页等等。它会向您打开浏览器。

这是非常强大的。不喜欢你的特定浏览器的书签模式？用 Python 写你自己的将是小菜一碟——你可以做更聪明的事情，比如应用一点机器学习来处理将它们分类。想要在每天的特定时间打开(或刷新)一组网页吗？Cron ，或者它复杂得多的对等物 [systemd](https://en.wikipedia.org/wiki/Systemd) ，几行代码就可以做到。想要为每个以“H”开头的网站制作一个将暗模式转换为亮模式以及将亮模式转换为暗模式的硬件按钮吗？可以做。

我挑的是浏览器，但许多大型软件都是以同样的方式无法访问的——即使它们是开源的，它们也没有开辟与用户代码或脚本交互的渠道。(一切“在云端”或者“作为服务”，我看着你呢！但这是另一天的进一步咆哮。)这很遗憾，因为这些“大”软件实际上做的是最酷的事情。

所以，如果你正在开发一个大的软件包，或者仅仅是为一个软件包写一个插件，*请*考虑一下你如何能让普通的脚本编写者获得更多的功能。否则，它只是塑料块，与该套件的其他部分不匹配。

This article is part of the Hackaday.com newsletter, delivered every seven days for each of the last 200+ weeks. It also includes our favorite articles from the last seven days that you can see on [the web version of the newsletter](https://mailchi.mp/hackaday.com/hackaday-newsletter-649368). Want this type of article to hit your inbox every Friday morning? [You should sign up](http://eepurl.com/gTMxQf)!