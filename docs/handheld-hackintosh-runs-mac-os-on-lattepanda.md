# 手持 Hackintosh 在 LattePanda 上运行 Mac OS

> 原文：<https://hackaday.com/2021/06/30/handheld-hackintosh-runs-mac-os-on-lattepanda/>

由于越来越强大的单板计算机的出现，在过去的几年里，我们已经看到了大量定制便携式计算机的涌入。其中绝大多数都是 ARM 驱动的，使用的是 Raspberry Pi 4 之类的东西，自然运行的是 Linux。只有少数几个在 x86 硬件上运行，通常是因为无论是谁构建了它，都希望能够运行 Windows。

但是这款运行最新 Mac OS 的 x86 手持电脑确实是独一无二的。创造者[iketsj]声称这是世界上第一个，经过一番搜索，我们倾向于同意。虽然其他人已经在 LattePanda 上安装了 Mac OS 来创建 Hackintosh 笔记本电脑，但这似乎确实是第一台利用这种特殊硬件和软件混合的*手持*电脑。

[![](img/35ea2d3d2ebb574bb1bc1257738c38c4.png)](https://hackaday.com/wp-content/uploads/2021/06/macdeck_detail2.jpg) 像我们看到的其他定制便携式电脑一样，这款电脑从 3D 打印外壳开始。整体设计[让我们想起了 YARH。我们去年报道过的 IO](https://hackaday.com/2020/09/03/yarh-io-is-the-hackable-pi-portable-of-our-dreams/)，甚至借用了其中一个微型键盘/指针组合的薄膜和 PCB 的技巧。在这种情况下，这一点尤为重要，因为为了与苹果自己的便携式 Mac OS 机器保持一致，这款手持设备的屏幕不支持触摸。

我们尤其喜欢 LattePanda 上集成的 Arduino 如何与一些 MOSFETs 结合使用，以控制手持设备的 LCD、键盘和风扇的电源。虽然这听起来像是风扇目前正在全速运转，[iketsj]提到他确实打算在未来增加自动速度控制。像这样的专用“机箱控制器”很有意义，并且我们认为随着这些可移植构建变得越来越复杂，它只会变得越来越普遍。

既然我们已经看到了运行 Mac OS 的定制便携式计算机，我们是否会在未来看到一个全新的 cyberdecks 运动库比蒂诺的软件？也许不是。正如[iketsj]在这个视频的结尾所指出的，[苹果从 x86 转向他们自己的芯片](https://hackaday.com/2020/07/13/changing-system-architectures-and-the-complexities-of-apples-butterfly-approach-to-isas/)几乎肯定会在未来几年内意味着 Hackintosh 项目的死亡，给[计算机黑客的迷人时代画上句号](https://hackaday.com/tag/hackintosh/)。

 [https://www.youtube.com/embed/_cdsdrqA-50?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/_cdsdrqA-50?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

