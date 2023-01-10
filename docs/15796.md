# 用 Gluon 把网页变成桌面应用

> 原文：<https://hackaday.com/2022/12/30/turn-a-webpage-into-a-desktop-app-with-gluon/>

Electron 是一款运行网络应用程序的软件，其运行方式与本地应用程序相同，而且由于其内存需求，该软件在这些方面受到了很多负面报道。但是，虽然执行可能会留下一些需要的东西，但这个概念本身是非常可靠的——如果您已经为 web 编写了代码，那么一种快速而简单的方法将它带到桌面上将是非常有价值的。

这就是为什么[CanadaHonk]正在构建一个名为 [Gluon](https://github.com/gluon-framework/gluon) 的框架，旨在不费吹灰之力将你的网页变成桌面应用。我们已经看到了他们几个月前在[open asar 项目中的工作，](https://hackaday.com/2022/06/19/openasar-tweaks-discords-frontend-improves-performance-and-privacy/)破解了 Discord 桌面应用程序来加速它。借鉴这一经验，Gluon 被打造为精益——应用程序具有低 RAM 和存储空间，闪电般的构建时间，以及严肃的 API。

最酷的部分之一是，它可以使用你的系统安装的浏览器，而不是像电子捆绑在一起。Firefox 支持也在路线图上，目前处于试验阶段。对 Linux 的支持也在进行中——这个框架是 Windows 生的，但这将会改变。还有创新的空间；[CanadaHonk]最近增加了一个休眠功能，当应用程序最小化时，它会积极减少 RAM 和 CPU 占用，这是其他类似框架所不知道的。

如果你想写面向用户的软件，JavaScript 是一种不错的语言，而且你们中的很多人会很熟悉它。你也不局限于技术世界的软件方面——像 WebUSB 和 WebSerial 这样的工具可以让你为你刚刚开发的主板编写用户界面。例如，这里有一个[基于网络串行的示波器](https://hackaday.com/2021/02/22/slick-web-oscilloscope-is-ready-in-a-flash-literally/)，一个漂亮的[串行终端](https://hackaday.com/2022/03/21/web-serial-terminal-means-its-always-hacking-time/)，或者一个黑客会议徽章[编程工具包](https://hackaday.com/2021/03/21/webserial-browser-based-development-for-your-boards-and-electronic-badges/)。尽管浏览器犯了很多错误，但它们似乎并没有变得更丰富，如果这意味着你可以快速开发跨平台的面向硬件的应用程序，这无疑是一个有用的补充。