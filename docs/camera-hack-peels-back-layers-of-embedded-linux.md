# Camera Hack 剥离嵌入式 Linux 的底层

> 原文：<https://hackaday.com/2021/04/20/camera-hack-peels-back-layers-of-embedded-linux/>

如今，嵌入式 Linux 设备无处不在，迟早，你会想要在其中的一个设备上闲逛。但是怎么做呢？这就是像菲利普·阿斯特罗萨这样的帖子出现的原因。虽然他的工作重点是 Foscam C1 安全摄像头，但他在这里概述的技术和工具将适用于所有以一只小企鹅为核心的设备。

[Felipe]没有试图从前门进入，而是从核选项开始了他的攻击:从相机的 PCB 上拆下 SPI MX25L12835F 闪存芯片，并用树莓 PI 倾倒其中的内容。从那里，他通过使用不同的工具来确定芯片的分区方案，并最终从内部的各种文件系统中提取密码和其他有趣的信息。

[![](img/26542ea770c8f2112881e5f874411b0a.png)](https://hackaday.com/wp-content/uploads/2021/04/linuxcam_detail.jpg)

Getting ready to remove the flash chip.

单单这一点就值得一读，但是一旦[费利佩]发现了`FirmwareUpgrade`计划，事情就真的变得有趣了。由于 Foscam 的软件更新是加密的，他认为对二进制文件进行逆向工程将会发现密钥，并允许创建自定义固件映像，这些映像可以通过 stock 接口进行刷新。

Ghidra 和朋友们的进一步调查发现了一个有趣的共享库，它与有问题的可执行文件相关联，然后为了弄清楚密钥是如何被混淆的，它被分解了。我们不会破坏这个惊喜，但是菲利普最终会得到他想要的。

这不是[【费利佩】第一次摆弄这些联网摄像头](https://hackaday.com/2014/11/11/how-to-backup-and-restore-your-ip-camera-firmware/)的固件，我们敢说这不会是他的最后一次。对于那些真正喜欢摆弄这类设备的人来说，[为闪存芯片](https://hackaday.com/2020/05/20/poking-around-inside-of-a-linux-security-camera/)安装一个插座以使软件修改更快更容易并不是什么新鲜事。