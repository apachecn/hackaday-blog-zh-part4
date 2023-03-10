# 树莓派浇灌你的草坪，提供 HTML

> 原文：<https://hackaday.com/2020/04/29/raspberry-pi-waters-your-lawn-serves-html/>

很容易拿一个树莓派，把它当成一个廉价的 Linux PC 或服务器。运行广告拦截器或 VPN 网关很简单，不需要任何真正的接口。然而，实际使用 Pi 来控制某些东西是一个很大的飞跃，一个好的例子可以帮助你开发你自己的项目。[Joeseph Luccisano]发布了一个具有这个目的的教程。目标是:建立一个低成本的草坪浇水系统。

这是一个有趣的项目，因为它有硬件和软件组件，当然。但它也有一个液压部分，所以你必须处理所有三个领域走到一起。

当然，你的院子会有所不同，所以如果你决定自己实现，一些设计会改变。然而，有很多关于他如何放置这些区域以及他为什么做出这些选择的信息。那应该是你自己设计的很好的基础。

看起来教程的软件部分是一个正在进行的工作。但基本思想是使用 Flask for Python 创建一个 HTTP 服务器，并公开一个基本的 Web API。一款名为 [Curler](https://apps.apple.com/us/app/curler-your-http-apis-interface/id1210896283) 的 iPhone 应用创建了一个好看的使用界面来调用 API。我们认为你可以在安卓系统上用 [HTTP 请求快捷方式](https://play.google.com/store/apps/details?id=ch.rmy.android.http_shortcuts&hl=en_US)，或者其他类似应用的 [any](https://play.google.com/store/apps/details?id=com.idlegandalf.httprequestwidget&hl=en_US) 做同样的事情。

当然，我们不能一想到洒水器就不去想那些[可怜的猫](https://hackaday.com/2016/07/08/neural-network-targets-cats-with-a-sprinkler-system/)。一旦你给你的草坪浇过水，你会想要[修剪草坪。](https://hackaday.com/2019/04/23/mowerbot-keeping-the-lawn-in-check-since-1998/)