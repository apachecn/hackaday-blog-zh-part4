# PineCube 手把手:一个开放的 IP 摄像头，乞求更好的内核支持

> 原文：<https://hackaday.com/2021/04/22/hands-on-with-pinecube-an-open-ip-camera-begging-for-better-kernel-support/>

当 Pine64 项目在 2020 年宣布 PineCube 时，它引起了相当大的兴趣。这主要是由于基于网络的(IP)相机外形中的单板计算机(SBC)的吸引力，该相机具有集成的相机模块，仅售 29.99 美元。给它加上一个外壳，你就会有一个整洁的小包装，结合了一个 5 MP 相机模块和 100 Mbit 以太网和 WiFi。此外，除了 MicroUSB 之外，该系统还可以通过可选的电池组和无源 PoE 供电。

几周前[我买了两块这样的板](https://pine64.com/product/pinecube-dev-kit/?v=0446c16e2e66)，作为客户项目的一部分，并着手用它来实现一个定制的 IP 摄像机。根据我现有的基于 SBC 的 Linux 和 MIPI (CSI)相机经验，从 Raspberry Pi 到 Odroid、Orange Pi 和 Banana Pi 板，我非常有信心可以让它工作起来毫不费力。

不幸的是，我的经历一点也不积极。在花了很多时间使用 PineCube 后，我无法向那些寻求 IP 相机的人推荐它。这有很多原因，我将在本文中尝试解释。

## 第一印象

[![](img/806775fe65ce5f17786a59b7fca15a78.png)](https://hackaday.com/wp-content/uploads/2021/03/pinecube_hands-on-6.jpg)

The front of the PineCube, with the lens cap removed.

订购这两块 PineCube 板(PineCubes？)是一种有点奇怪的体验，即使一个人习惯于在网上订购硬件。点击 Pine64 商店中的对话框并支付订单后(选择标准运输)，我收到了一封确认电子邮件。没有预计的发货日期，但在等待了几个星期后，我想知道我是否会得到更新，我收到了一个通知，我的订单已经发货，以及一个跟踪链接。

这种追踪在海关办公室的某个地方结束，所以有一天我突然收到了装有松果的包裹。在这个普通的纸箱里有两个白色的小盒子，每个盒子里都有一个松木盒子。在拆箱过程中，我担心在从软袋中取出装置时会扯下一些电线或软电缆。

[![](img/9938b715c9d238987a5f5992a692914f.png)](https://hackaday.com/wp-content/uploads/2021/03/PinecubeCase1.jpg)

The enclosure for the PineCube which one cannot get. Yet.

扬声器模块悬挂在两根相当长的电线的末端，我觉得有必要检查连接组成系统的两块板的扁平软线(双板计算机是一个术语吗？)，以防它移位。它不像是你想经常处理的那种板，就像树莓派或类似的东西。它感觉很脆弱，你希望你能马上把它放进围栏里以保证它的安全，但没有真正稳定的方向来把它放在桌子上。

由于 [PineCube Wiki](https://wiki.pine64.org/index.php?title=PineCube) 页面包含一个链接，该链接应该是稍后将被出售的案例的 STL 文件——根据[最近的一篇博客文章](https://www.pine64.org/2020/12/15/december-update-the-longest-one-yet/)——我想在电路板到达这里之前，我会在我放在这里的 3D 打印机上打印一份副本。不幸的是，正如人们在那篇博文的评论中指出的，没有发布 STL 文件，而是发布了专有的 SolidWorks CAD 文件。三个月后仍然没有可用的 STL 文件(**更新**:在撰写和发布这篇评论之间增加了一个“快速和肮脏的 STL 转换”)。还没有附件出售。

## 停产传感器和 Linux 支持

[![](img/7ad4b67d8f33c66f042b9303b84bcdc7.png)](https://hackaday.com/wp-content/uploads/2021/03/pinecube_hands-on-7.jpg)

There is a GPIO header that provides a UART, SPI, I2C and such as well.

由于机箱只是大图中的一个“很好”的细节(双关语)，所以我将重点放在我收到的硬件的功能部件上。看到这款相机是一款 [OV5640](https://www.ovt.com/sensors/OV5645) 相当令人失望，这是一款大约有 9 年历史的传感器，已经停产有一段时间了。这使得 PineCube 的未来看起来相当可疑，而且可能是短暂的。

从好的方面来看，这也意味着 Linux 下对它的支持没有问题，当使用 ffmpeg 设置 RTMP 流时，Video4Linux (v4l)很乐意接受它作为输入源。然而，这与 S3 SoC 中 GPU 的情况截然不同。正如你在 Linux-孙茜的“ [Linux 主线任务](https://linux-sunxi.org/Linux_mainlining_effort)”页面上看到的，Linux 内核 5.11 是第一个将 S3 支持列为已合并的版本。内核 5.10 中的 S3 支持是通过 V3s SoC 支持来完成的，当查看使用内核 5.10 的 PineCube 的 [Armbian 中的硬件覆盖文件时可以看出这一点。S3 和 Allwinner V3 SoCs 都是派生的，所以有些兼容性是有意义的。](https://www.armbian.com/pinecube/)

[![](img/1ab5ba2d989c750511333a733785542e.png)](https://hackaday.com/wp-content/uploads/2021/03/pinecube_hands-on-3.jpg)

A look inside the PineCube. Notice the easily damaged wires.

此时，视频编码仍在进行中。这意味着 ffmpeg、gstreamer 或任何用于视频编码的图形框架都必须在软件中完成所有这些工作，使用单个 Cortex-A7 CPU 内核和 NEON 矢量处理扩展。从相机中得到一个简单的 RTMP 流，这似乎已经足够了。

如前所述，PineCube 还有一个扬声器。遗憾的是，由于没有注册音频设备，目前无法使用。这种支持可能会在下一个 Armbian 版本中出现，但是，由于最近[贡献了](https://github.com/armbian/build/pull/2727)一个改进的硬件覆盖修复。

## 用作照相机

在一般情况下，PineCube 与其他 SBC 非常相似。在打开系统之前，下载目标板的图像，将其写入 MicroSD 卡，并将其插入板的 MicroSD 读卡器。由于 PineCube 没有视频输出，交互方法仅限于串行连接或 SSH(如果连接到以太网)。使用任何一种方法建立控制台连接后，登录 Armbian 就像 1234 一样简单。(这是默认的 root 密码。)

登录 Armbian 后，只需安装 media-ctl(包 v4l-utils)和 ffmpeg，就可以设置 RTMP 流，然后运行以下命令，为 RTMP 服务器设置 640×480 FLV 编码的流:

```
$ media-ctl --set-v4l2 '"ov5640 1-003c":0[fmt:UYVY8_2X8/640x480@1/15]'
$ ffmpeg -s 640x480 -r 15 -i /dev/video0 -vcodec flv -f flv rtmp://<rtmp_server>/live/pinecube
```

运行该命令并通过桌面系统的播放器连接到 RTMP 服务器后，现在可以在 glorious 640×480、每秒 15 帧的分辨率下观看 PineCube 中的视频，只有几秒钟的延迟。在 1080p 时，FPS 可以增加到 30 FPS，但如果没有硬件编码支持，这可能会导致断断续续和毛刺。

在设置系统时，我注意到它在通过 HTTP 下载一些资源时会可靠地挂起，并且只有在 HTTP 下载超时后才会再次恢复。当我在另一个 SSH 终端中打开`top`时，我可以看到系统负载上升到 12 甚至更多，因为系统的 111 MB RAM(总共 128 MB)和交换空间都被填满了。

当我试图建立一个添加了更多本地处理(h.264 编码)和自定义安全层(加密)的 RTMP 流时，同样的模式再次出现。如果没有硬件编码支持，我可以看到系统负载飙升，直到系统停止响应。在大约 10 分钟的延迟后，通过 SSH 终端发送 Ctrl+C 终于成功了。

## S3 足球俱乐部

[![](img/41cbe85c7ec1eb5463ed9603a861cc51.png)](https://hackaday.com/wp-content/uploads/2021/03/pinecube_hands-on-4.jpg)

The S3 SoC can be spotted deep inside the PineCube stack.

当我将 PineCube 与我合作过的其他 SBC 进行比较时，这种特定主板上的 S3 SoC 似乎是主要的限制因素，尤其是 RAM 量低和持续缺乏硬件支持。它似乎首先是一款针对低成本 IP 摄像机的 SoC，这意味着试图超越这种专注带来的限制将会带来反响。

在这方面，令人感兴趣的是，Olimex 也计划在今年以 S3-奥利努辛诺的形式发布一个总部设在 S3 的董事会。也许有更多像这样的开源板有助于增加对这些更模糊的 SOC 的支持。我清楚的是，如果没有完整的硬件支持，特别是对视频编码的支持，这些平台的使用将会受到限制。

## 包扎

对于更普通的用户，我可能会将 30 美元的 PineCube 与上述考虑进行比较，以及类似树莓 Pi Zero W(18 美元)或[香蕉 Pi M2 Zero](http://www.banana-pi.org/m2z.html)(H2+SoC，25 美元)，以及类似[树莓 Pi V2 相机](https://www.raspberrypi.org/products/camera-module-v2/)模块和索尼 IMX219 8 MP 相机模块(25 美元)。不到 50 美元，你就可以拥有一个内存更大的主板(甚至 RPi Zero 也有 512 MB)，一个更好的摄像头，以及随时购买或打印附件的选项(包括摄像头模块)。

Allwinner H2+和 Raspberry Pi Zero 的 BCM2835 SoCs 多年来一直支持主流 Linux，包括视频编码等内容。所有这一切让人不禁想知道，松果立方的存在理由到底是什么，以及 S3 足球俱乐部在更普遍的环境中的存在理由。

至于我购买这些 PineCube 板的更专业的设置，我相当有信心它可以工作，并且很可能大多数挥之不去的问题和硬件支持方面的差距将随着时间的推移得到解决。然而，在这次经历之后，我确实觉得，对于那些不愿意投入大量时间来完成哪怕是最基本的事情的人来说，这不是一个合适的平台。