# 使用 Umbrel 实现更轻松的自助托管

> 原文：<https://hackaday.com/2022/07/09/easier-self-hosting-with-umbrel/>

虽然不可否认的是，基于云的服务很方便，但还是有人宁愿自己做。对我们许多人来说，这是因为我们想要我们想要的方式。对于另一些人来说，这是一种不信任，因为他们把自己的个人数据放在自己无法控制的服务器上。Umbrel 是一个 Linux 发行版,只面向那些希望自己托管流行应用程序(如 NextCloud 或 Home Assistant)的人。[ItsFoss]有一篇很好的评论，指出了 Umbrel 早期版本的一些优缺点。

然而，真正有趣的是发行版安装软件的方式。像大多数现代发行版一样，Umbrel 有一个包管理器。然而，与大多数不同的是，这些包实际上是 docker 容器。因此，当你安装一个应用程序时，它是预先配置好的，存在于自己的气泡中，不太可能与你可能安装的其他东西发生冲突。

我们还喜欢它有一个特定的 Raspberry Pi 构建，尽管它可以在其他 64 位硬件上工作，你甚至可以在普通操作系统之上的 docker 中安装它。当然，docker 容器的概念也是一个缺点——至少目前是这样——因为与更传统的安装方式相比，很难调整容器内部的设置。

令我们惊讶的是，硬件已经变得如此强大，以至于复制整个操作系统比解决所需的依赖交互更容易。尽管如此，它还是有效的，而且在大多数情况下，它都是有效的。

如果你想了解更多关于 [Docker](https://hackaday.com/2018/09/05/intro-to-docker-why-and-how-to-use-containers-on-any-system/) 的信息，我们过去已经报道过几次了。如果你愿意，你甚至可以[用它来处理非常简单的开发案例](https://hackaday.com/2022/06/21/linux-fu-docking-made-easy/)。

 [https://www.youtube.com/embed/Uu1TuE6RdKM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Uu1TuE6RdKM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

