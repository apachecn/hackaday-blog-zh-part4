# 宋承宪很神奇，但是隧道更好

> 原文：<https://hackaday.com/2022/04/24/ssh-is-magic-but-tunnels-are-even-better/>

从前，几年前我在一家酒店做硬件安装的现场支持。远程技术人员的远程桌面软件不想在我的 Linux 笔记本电脑上运行，所以他无法进入他需要配置的交换机来进行安装。我问他是否有他可以使用的 SSH 端口，如果他和我在房间里的话。当然了，但这对他没什么好处。我运行了一个到我的公共服务器的反向 SSH 隧道，并将其指向本地端的交换机。我说服他在给定的端口上 SSH 到我的服务器，他神奇地连接到了他的交换机。他真的对这种伎俩感到敬畏，并要求知道如何做到这一点。SSH 是不可思议的，但是通过 SSH 进行流量隧道传输是非常神奇的。[Shawn Powers]同意了，并且[决定帮助我们其他人理解这个过程](https://www.youtube.com/watch?v=Wp7boqm3Xts)。


有两种启动隧道的基本方法，第一种是本地隧道，它在本地机器上侦听，并将其转发到远程机器。另一方面，远程隧道将侦听远程机器，并将流量传送到本地机器。当您有多个 SSH 会话，并将一个隧道连接到另一个隧道，将某些东西路由到您需要的地方时，真正的乐趣就开始了。要额外加分，请查看隐藏的 SSH 命令行，按 Enter 键，然后按`tilde`和`C`键，一次一个键。另外，为了额外加分，请查看[Shawn]的其余 Linux 内容，以了解一些额外的 Linux 优点。

 [https://www.youtube.com/embed/Wp7boqm3Xts?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Wp7boqm3Xts?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

