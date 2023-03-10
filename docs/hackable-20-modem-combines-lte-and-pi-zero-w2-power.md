# 可破解的 20 美元调制解调器结合了 LTE 和 Pi Zero W2 功率

> 原文：<https://hackaday.com/2022/08/03/hackable-20-modem-combines-lte-and-pi-zero-w2-power/>

[extrowerk] [告诉我们一种新的黑客友好设备](https://extrowerk.com/2022/07/31/OpenStick/)——一个 20 美元的 LTE 调制解调器棒，带有四核 CPU 和 WiFi，能够运行全功能的 Linux 发行版。这一发现依赖于一位中国黑客[【帅气的燕燕】](https://github.com/HandsomeYingyan)的大量工作，他发现这种棍子运行安卓系统，[破解了它的引导加载程序，](https://github.com/OpenStick/lk2nd)为它调整了[一个 Linux 内核](https://github.com/OpenStick/linux)，而[为这种棍子创建了一个 Debian 发行版](https://github.com/OpenStick/OpenStick/releases)——称之为 OpenStick 项目。[extrowerk]的文章为我们翻译了[帅妍]的教程，并做了一些更有用的笔记。有了这篇文章在手，我们已经解锁了一个全新的 SBC 用于我们的项目——价格低得惊人！

有时甚至最简单的π0 都不存在(又一次！)，这是一个奇妙的发现。花比零 2W 多一点的价格，你就可以买到一台具有类似 CPU(基于 4 核 1GHz A53 的高通 MSM8916)、相同内存、4GB 存储、WiFi 和 LTE 调制解调器的计算机。你可以把它插在一个 powerbank 或 wallwart 上，在一个远程位置运行它，使它成为一个家庭自动化中心，或者在一个小空间内处理一些 CPU 密集型任务。你甚至可以通过 microSD 插槽获得额外的存储空间，或者甚至是额外的 GPIOs？你不会得到一个焊接友好的 GPIO 头，但它有几个 led，显然，一个 UART 头，所以这并不都是坏的。正如[extrowerk]所指出的，这基本上是一部棒形手机，但没有显示屏和电池。

现在，有一些警告。[extrowerk]指出，您应该购买适合您所在国家的 LTE 频段的调制解调器，这不是唯一需要注意的事情。我们的一个朋友最近得到了一个视觉上相同的调制解调器；当我们得到这个黑客的消息时，她为我们拆开了它——发现它配备了一个更有限的 CPU，MDM9600。那是一个 LTE 调制解调器芯片，它的功能仅限于执行 USB 4G 棒任务和一些基本的 WiFi 功能。根据一个流行的移动设备逆向工程论坛的[调查](https://4pda.to/forum/index.php?s=&showtopic=849043&view=findpost&p=110522968)(俄语，[翻译](https://4pda-to.translate.goog/forum/index.php?showtopic=849043&st=1440&_x_tr_sl=auto&_x_tr_tl=en&_x_tr_hl=en#entry110522968))，看起来这款调制解调器的早期版本采用了更有限的 MDM9600 SoC，无法像我们感兴趣的 stick 一样运行 Linux。如果你喜欢这种调制解调器，并且可以理解地想购买一些，看看你是否能确保你将得到 MSM8916 而不是 MDM9600。

自从 Raspberry Pi 出现以来，使用 WiFi 路由器为我们的机器人提供动力的日子已经一去不复返了，但我们仍然深情地记得它们，我们很高兴看到路由器坚持使用 Pi 零 2W 的魅力。我们在这方面已经做了五年多了，大部分基于 [OpenWRT，](https://hackaday.com/2019/02/01/this-tiny-router-could-be-the-next-big-thing/)一些像[SD 读卡器一样小。](https://hackaday.com/2016/01/27/cheap-wifi-devices-are-hardware-hacker-gold/)现在，当 SBC 很难获得时，这可能是你下一个项目的绝佳选择。

**更新:**在下面的评论中，人们发现了一些链接，在这些链接中，你应该能够获得一个带有正确 CPU 的调制解调器。另外，[乔]和[已经开始调查船上的部件了！](https://www.zianet.com/jgray/openstick/)