# 一个平民预算的移动信号黑客

> 原文：<https://hackaday.com/2019/06/05/mobile-sigint-hacking-on-a-civilians-budget/>

信号情报(SIGINT)是指通过窃听通信来进行电子侦察，过去这种事情只属于军方或各种三字母政府机构的权限范围。但是今天，不管是好是坏，单个黑客已经能够利用低成本的硬件和开源软件从空气中获取大量的信息。现在，多亏了[乔希·康威]，所有这些能力[都可以用一个精巧的一体化设备加以利用:放射性同位素探测仪](https://gitlab.com/crankylinuxuser/siginttablet)。

在最近的 2019 CircleCityCon 上的演讲中，[Josh](也称为[CrankyLinuxUser])介绍了 RadioInstigator，这是一种超越传统 WiFi 和蓝牙进入无线安全研究世界的廉价方式。确切地说，该设备内部的硬件没有一个是新的，它都是黑客社区已经访问了一段时间的东西，但这个项目将它们都集中在一个 3D 打印的“屋顶”下。最终的结果是一个看起来非常实用的设备，可以在旅途中使用，以大约 150 美元的成本探索巨大的射频频谱。

[![](img/4db11f99f72779bbddce436f379286d2.png)](https://hackaday.com/wp-content/uploads/2019/06/instigator_detail.jpg) 那么【乔希】在这个无线玩具盒里装了什么？人们可能不会惊讶地发现，该展会的明星是 Raspberry Pi 3 B+，结合了触摸屏显示器和便携式键盘，因此用户可以与安装的各种安全工具进行交互。

为了帮助 RadioInstigator 在电波中冲浪，有一个 RTL-SDR 和一个 2.4 Ghz NRF 24 Lu 1+“crazy radio”，两者都在设备外部连接到外部天线连接器。甚至还有一个外部 SMA 连接器连接到 Pi 的 GPIO 引脚，可用于 5 KHz 至 1500 MHz 的低功耗传输，支持 rpitx。一切都由一个强大的 10，000 毫安的电池组供电，这应该给你足够的时间来执行你的调查。

[Josh]还写了几个 Bash 脚本，这些脚本将自动在 Pi 上安装大量的无线电黑客工具，要么通过官方存储库下载它们，要么下载源代码并编译它们。让软件环境进入一个已知良好的状态可能会耗费大量的时间，所以即使您没有构建自己版本的 RadioInstigator，他的脚本仍然值得一试。

你只需要一个 Pi 和一个 RTL-SDR 就可以做一些[非常不可思议的事情，但是我们不禁注意到 RadioInstigator 内部仍然有足够的空间来容纳更多的设备。它可能是](https://hackaday.com/2017/09/10/attack-some-wireless-devices-with-a-raspberry-pi-and-an-rtl-sdr/)[多 RTL 设置](https://hackaday.com/2017/01/30/gsm-sniffing-on-a-budget-with-multi-rtl/)的完美家园，或者[甚至可能是一个用于欺骗手机网络的 VGA 适配器](https://hackaday.com/2018/04/23/spoofing-cell-networks-with-a-usb-to-vga-adapter/)。

 [https://www.youtube.com/embed/Hyq6_IZ-2fE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Hyq6_IZ-2fE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

