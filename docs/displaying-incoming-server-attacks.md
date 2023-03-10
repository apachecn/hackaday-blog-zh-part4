# 通过给服务器日志一个记分板来显示传入的服务器攻击

> 原文：<https://hackaday.com/2020/09/23/displaying-incoming-server-attacks/>

在服务器领域，如果不需要，端口不应该暴露在更大的互联网中，这是一个必然的结论。到处都有恶意机器人，它们会尝试并随机访问任何连接到网络的东西，最好的办法就是完全关闭它们。如果您必须打开一个端口，比如 SSH 的 22 端口，那么就需要对它进行适当的保护和监控，以便管理员能够跟踪它。通常这是在系统日志中完成的，并放在一边，但[Nick]想要[一个更提前的提醒，告诉他有多少次尝试登录他的系统](https://nick-web.co.uk/raspberrypi/posts/2020-09-21/pialert)。

这个构建主动监视在端口 22 上登录到他的服务器的尝试，并通过数字显示和一系列 led 通知他。它基于 3D 打印外壳中的 Raspberry Pi Zero W，通过与服务器上运行的一个名为`fail2ban`的程序进行交互来工作。`fail2ban`的主要工作是阻止在服务器上登录失败一定次数的 IP 地址，但作为自由/开源软件，它可以针对这种情况进行修改。通过在 Pi 上运行一些 Python 代码，它能够收集来自`fail2ban`的数据并显示出来。

[Nick]也能看到立竿见影的效果。在 24 小时内，他在启用正常登录的服务器上看到了 1633 次登录尝试，这立即显示在显示器上。下面链接了一段计数器运行的视频。但是，如果您需要服务器上的实时信息，您并不总是需要辅助显示器。[这个 Pi 服务器有自己的内置显示器](https://hackaday.com/2020/09/01/a-cyclopic-lcd-case-for-your-raspberry-pi-server/)。

 [https://www.youtube.com/embed/KPyegtEO4iE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/KPyegtEO4iE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

