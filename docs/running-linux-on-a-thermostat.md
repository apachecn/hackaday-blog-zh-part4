# 在恒温器上运行 Linux

> 原文：<https://hackaday.com/2019/06/10/running-linux-on-a-thermostat/>

当你的恒温器上运行 Linux 时，那就不是黑客了。如果没有，而你自己在上面安装了 Linux，那么它肯定是存在的。这正是[cz7asm]所做的。在最近的一个视频中，他展示了霍尼韦尔恒温器启动 Linux 并运行各种软件。

虽然恒温器内部的硬件不能提供典型的现代嵌入式 Linux 的所有奢侈品，但它为基本功能提供了足够的空间。该系统从 RAM 中的 1 MB rootfs 运行，并有一个 2.5 MB 的内核映像，剩余 12 MB 用于其他所有内容。凭借这些微薄的资源，[cz7asm]展示了该系统如何使用 USB 网络适配器，连接到[telehack.com](http://telehack.com)以获得一些命令行复古乐趣，并托管 web 服务器，尽管还没有浏览器运行。还有显示图形和动画的帧缓冲支持，以及通常的 Linux 终端优点。

到目前为止，我们只看到了视频，所以我们希望[cz7asm]在某个地方发布代码，因为我们已经厌倦了使用我们的恒温器来运行 AC。

你可能还记得[cz7asm]之前的恒温胜利: [running Doom](https://hackaday.com/2017/05/22/doomed-thermostat/) 。休息过后，请观看最新的恒温器冒险视频。

感谢[Piecutter]的提示！

 [https://www.youtube.com/embed/iQKnL692q0w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/iQKnL692q0w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

