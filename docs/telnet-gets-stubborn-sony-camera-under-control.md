# Telnet 控制住顽固的索尼摄像机

> 原文：<https://hackaday.com/2022/11/25/telnet-gets-stubborn-sony-camera-under-control/>

据 LinuxGameCast 的技术制作人【Venn Stone】称，尽管索尼 a5000 早在 2014 年就发布了，但对于那些希望拍摄 1080p 视频的人来说，它仍然是一个可靠的选择。虽然这款相机重量轻，价格实惠，但它也有一些令人讨厌的怪癖——即 HDMI 输出上的覆盖层(如上图所示)，无法使用相机的正常配置菜单关闭。但是碰巧的是，使用一些开源工具和古老的 telnet，[你实际上可以登录相机的操作系统，直接调整它的设置](https://linuxgamecast.com/2022/11/sony-a5000-clean-hdmi-hack-power-off-bypass/)。

正如文章中所解释的，第一步是安装[索尼-PMCA-RE](https://github.com/ma1co/Sony-PMCA-RE) ，这是一个为逆向工程和修改索尼相机而开发的跨平台工具套件。通过 USB 连接相机，这将允许你在相机上安装一个名为*的程序打开记忆调整*。这解锁了相机上的一些开发者选项，例如在其 WiFi 接口上生成 telnet 服务器。

[![](img/5f9bd4db24831de5a318581907449b75.png)](https://hackaday.com/wp-content/uploads/2022/11/a5000_detail.jpg) 随着 a5000 连接到您的无线网络，您将 telnet 客户端指向它的 IP 地址，就会看到一个 BusyBox 界面，玩过嵌入式 Linux 小工具的人应该都很熟悉。最后一步是调用适当的命令`bk.elf w 0x01070a47 00`，将摄像机配置文件的具体地址设置为零。这将永久禁用 HDMI 覆盖，但可以通过再次运行该命令并将字节设置回 01 来恢复。

如你所料，索尼-PMCA-RE 软件包不仅仅能够解锁一个远程登录服务器。虽然它可能不如[固件修改强大，如佳能硬件](https://hackaday.com/2015/04/04/magic-lantern-brings-linux-to-canon-eos-cameras/)的 Magic Lantern，但那些寻找不会倾家荡产的可破解相机的人可能希望查看该项目的文档，看看还有什么可能。

 [https://www.youtube.com/embed/8M4hR9HiOzM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/8M4hR9HiOzM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[Aaron]的提示。