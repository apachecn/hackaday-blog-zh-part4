# 任何平台的轻量级操作系统

> 原文：<https://hackaday.com/2021/03/22/lightweight-os-for-any-platform/>

Linux 已经有了很大的发展，用户不得不从头开始编译内核和所有其他源代码，通常没有任何互联网连接来帮助编写文档。那是 Linux 的蛮荒之地，虽然如果我们需要的话，我们都可以依赖一个易于安装的 Ubuntu 发行版，但仍然有一些发行版需要发现那些旧的根源。见见 SkiffOS，[一个轻量级的 Linux 发行版，它可以在几乎任何硬件上编译](https://github.com/skiffos/skiffos),但也为容器化打开了一个充满机会的世界。

该操作系统旨在能够在任何兼容 Linux 的主板上进行自我编译(通过一些输入)，并且仍然是轻量级的。它可以在 Raspberry Pis、Nvidia Jetsons 和 x86 机器上运行，并专注于托管独立于其安装硬件的容器化应用程序。该操作系统的目标之一是将硬件支持与应用程序分离，同时能够支持实时任务，如机器人应用程序。它还使升级基本操作系统变得容易，而不会中断容器中运行的程序，当然还有容器化的所有其他好处。

看起来容器化确实是未来的发展方向，虽然它显然已经在虚拟主机和其他网络应用中得到了很好的应用，但是看到它扩展到实时领域还是很有趣的。大概像这样的方法会有许多其他应用，因为它不是特定于硬件的，我们很高兴看到未来的发展，因为人们会根据自己的特定需求采用这种类型的操作系统。

感谢[基督教]的提示！