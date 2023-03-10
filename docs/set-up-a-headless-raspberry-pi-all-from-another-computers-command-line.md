# 设置一个无头的 Raspberry Pi，全部来自另一台计算机的命令行

> 原文：<https://hackaday.com/2018/11/24/set-up-a-headless-raspberry-pi-all-from-another-computers-command-line/>

安装一个 Raspberry Pi 和在任何其他计算机上安装一个操作系统是有区别的，但是有一点是相同的，如果你做了足够多的工作，你会想尽一切办法来自动化这个过程。这就是[Peter Lorenzen]发现自己所处的情况，他的解决方案是[一个 shell 脚本来安装和配置 Raspberry Pi 进行无头操作](http://peter.lorenzen.us/linux/headless-raspberry-pi-configuration)，在这个过程中不需要连接键盘或显示器。

[Peter]的工具是一个名为`rpido`的脚本，有了它，为 headless 操作设置一个新的 Raspberry Pi 的过程变得非常简单。要建立一个新的 Pi，[Peter]需要做的就是:

1.  给他的笔记本电脑插个 SD 卡(正好运行 Ubuntu。)
2.  Run: `rpido -w -h myhostname -s`下载并安装最新版本的 Raspbian lite，进行一些基本的设置(比如设置主机名)，配置 headless 操作，并启动一个根 shell。
3.  使用根 shell 做任何进一步的调整或检查(比如启动`raspi-config`进行额外的修改。)
4.  退出 shell，从他的笔记本电脑中取出 SD 卡，并将该卡安装到 Raspberry Pi 中。

与逐步完成操作系统安装和设置任务的清单相比，[Peter]的脚本有明显的优势，更不用说不需要插入键盘和显示器的优势了。神奇的是[Peter]正在 chroot 环境中安装 SD 卡的文件系统。有了合适的工具，用于 Pi 的 ARM 二进制文件可以在他的(英特尔)Ubuntu 笔记本电脑上运行。在 SD 卡进入 Pi 的新家之前，用这种方式修改 sd 卡的内容要方便得多。

然而，并不是一切都必须围绕 SD 卡。[Jonathan Bennet]展示了通过使用 PXE 引导功能，在没有 SD 卡的情况下运行 Raspberry Pi 是可能的，允许它从同一网络上的服务器而不是存储卡引导和加载其文件系统。