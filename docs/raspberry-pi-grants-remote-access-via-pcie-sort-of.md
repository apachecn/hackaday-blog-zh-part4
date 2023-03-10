# Raspberry Pi 允许通过 PCIe 远程访问(某种程度上)

> 原文：<https://hackaday.com/2022/09/20/raspberry-pi-grants-remote-access-via-pcie-sort-of/>

[Jeff]在一个奇怪的地方发现了一个 Raspberry Pi——嗯，无论如何是计算模块版本——在[一个 PCI Express 卡](https://www.jeffgeerling.com/blog/2022/blikvm-pcie-puts-computer-your-computer)上。你为什么要把树莓派插在电脑上？你并不完全是。该卡使用 PCI Express 连接器作为安装在计算机中并连接到 PC 接地的一种方式。Pi 暴露自己的网络电缆，由 PoE 或 USB C 电缆供电。那么它是做什么的呢？它提供远程键盘、视频和鼠标(KVM)服务。诀窍在于，即使您需要访问 BIOS 设置屏幕或对无法启动的操作系统进行故障排除，您也可以远程访问 PC。

这不是一个新想法。事实上，我们之前已经见过底层的 [Pi-KVM](https://hackaday.com/2020/11/24/true-networked-kvm-without-breaking-the-bank/) 软件，所以如果你不介意为 Raspberry Pi 找出你的安装选项，你可能不需要这个板。也是好事。从评论来看，实际上很难买到——也许是因为芯片短缺。

虽然拥有一个不依赖于复杂软件(甚至不依赖于您使用的操作系统)的远程解决方案似乎很有吸引力，但[Jeff]指出，延迟相对较高，因此您可能不会喜欢它用于任何游戏或视频。但这不是它真正的目的。

不过，这的确让我们思考。PCI Express 有 12V 和 3.3V 电源和接地连接。有些主板甚至在电脑关机时提供 3.3V。用这些东西你还能在电脑里装什么？或者用这张 Pi 卡你还能做什么？也许是联网的 USB？

我们已经看到一个 Pi 也包含了 PCI 总线。或者，你可以选择[更简单的手术方法](https://hackaday.com/2020/07/01/adding-pcie-to-your-raspberry-pi-4-the-easier-way/)。虽然将这些 KVM 板中的一个插入修改过的 Pi 是没有意义的，但我们也认为这会很有趣。

 [https://www.youtube.com/embed/cVWF3u-y-Zg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/cVWF3u-y-Zg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

