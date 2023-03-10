# 计算模块成熟了:向真正的前沿 Raspberry Pi 问好

> 原文：<https://hackaday.com/2021/10/14/the-compute-module-comes-of-age-say-hello-to-the-real-cutting-edge-of-raspberry-pi/>

如果我们想为我们的社区指出一个划时代的时刻，我们会带你回到 2012 年 2 月 29 日。这一天，剑桥一家小公司将他们的第一批新产品投放市场。这套设备就是后来的 Raspberry Pi Foundation，该产品是他们第一台单板计算机 Raspberry Pi Model B 的 10，000 个中国制造版本。凭借 BCM2835 SoC 和 512 兆内存，它可能不是第一个可以从 SD 卡运行 Linux 发行版的主板，但肯定是第一个以零花钱的价格这样做的主板。早在 2012 年的那个早上，对这种新主板的意外需求导致两家电子产品经销商的网站瘫痪，一款如今已成为传奇的产品诞生了。我们现在在 Model B 的第 4 版上，规格几乎在所有方面都进行了升级，更接近原版的东西仍然可以以其苗条的稳定体形式买到，即 Pi Zero。

## 你如何进化而不伤亡？

[![The original Pi Model B+ from 2014.](img/241b43a428bdb08b365e2b7afaf77d6c.png)](https://hackaday.com/wp-content/uploads/2021/09/1280px-Raspberry_Pi_B_top.jpg)

The original Pi Model B+ from 2014\. The form factor has had a few minor changes, but hardware-wise the Pi 4 follows this pretty closely. Lucasbosch, [CC BY-SA 3.0](https://commons.wikimedia.org/wiki/File:Raspberry_Pi_B%2B_top.jpg).

产生如此成功的产品线的问题是:这么多竞争对手和复制品紧随其后，你如何改进它？公平地说，有时它的竞争对手已经生产出比目前的 Pi 更强大的硬件，但他们没有剑桥的王牌:其独特的良好支持的 Linux 发行版，Raspberry Pi OS。正是这种强大的董事会和操作系统的结合，以及最少的冲击和惊喜，使得 Pi 在这么多年后仍然是人们追求的目标。

尽管如此，Pi 仍然是一个接口和 PCB 基本相同的 Pi，与最初的 Model B 第一次升级到 40 针插头和 4 个 USB 端口时一样。如何在不破坏与近几十年的项目的兼容性的情况下改进它呢？我们不知道 Pi 的人们对未来 Pi 5 的想法，但是我们想提出他们已经这样做了的理论，并且用了一个树莓 Pi。不是非常可爱的 Raspberry Pi 400 一体机，而是 Pi 4 的精简版兄弟，计算模块 4。向 Raspberry Pi 的新前沿问好，我们认为这是该平台目前最有趣的硬件开发。

[![The original StereoPi board](img/a864424dda05190dfa952ef88fdd2393.png)](https://hackaday.com/wp-content/uploads/2018/12/raspberry-pi-stereopi.jpg)

The original StereoPi board is a relatively rare project creating a custom board that’s visibly a Raspberry Pi,using an earlier Compute Module.

自 2014 年第一个以 BCM2835 的形式出现在 SODIMM 外形规格上以来，一直有 Raspberry Pi 计算模块出售。从那时起，我们已经看到了几个版本的 Raspberry Pi 3 的多核 BCM2837 仍然在 SODIMM 上，但公平地说，除了一些非常明显的例外，如 StereoPi，他们未能在我们的社区中引起轰动，而 Compute Module 4 在短时间内产生了一系列有趣的载板。

我们想冒险猜测一下为什么会出现这种情况，其中之一是早期的计算模块定价不是针对个人的，Zero 提供了一种更实惠的方式来找到更小 PCB 上的 Pi，尽管计算模块有能力，但它可能无法提供常规 Pi 无法提供的足够多的额外功能。这对于它最初瞄准的批量制造商来说是有意义的，但对于硬件黑客来说就不那么有意义了，因为 Pi 本身很容易获得。相比之下，子板格式的计算模块 4 提供了简单的可用性和一些非常美味的额外接口，如 PCI Express 总线，这使其成为比常规 Pi 更有吸引力的实验目标。当你可以按照自己的规格设计自己的圆周率时，为什么还要回头看呢？这里有几个例子，如果你不相信的话。

## 有太多的方法来旋转你自己的 Pi

[![Timonsku's minimal CM4 carrier board](img/5292be103410d47ec715ea757157b2d8.png)](https://hackaday.com/wp-content/uploads/2020/11/cm4carry800.jpg) 

【泰蒙斯库】的单面极小 CM4 载板

制作一个复杂的 PCB 对于我们这些不是每天以此为生的人来说往往是一个令人望而生畏的前景，所以我们来自【泰蒙斯库】的第一个 CM4 板[表明一个 CM4 项目根本不需要复杂](https://hackaday.com/2020/11/13/easy-carrier-board-for-the-compute-module-4-shows-you-can-do-it-too/)。这是一个 CM4 载板，带有全尺寸 HDMI 插座、USB-A 和 C 端口以及 microSD 插槽。当然，这是一个适中的规格，但它的与众不同之处在于 PCB 本身。这是一个单面设计，铣有 PCB 路由器，表明 CM4 载体非常简单，可以在家里制作。任何人真的可以旋转自己的圆周率！然而[Timonsku]并没有满足于他的荣誉，他还生产了 Piunora，一种采用 Arduino 足迹的 CM4 载体 T10。[![CM4-based NAS with PCIe](img/9eb374b0bdea8c43a10ddfa8d57be364.png)](https://hackaday.com/wp-content/uploads/2021/09/pi-cm4-nas.jpg)

This CM4 NAS carrier board brings out the PCIe interface to great effect.

[Arturo182]的[最小的 CM4 载板](https://twitter.com/arturo182/status/1429907175938437124)也是如此，尽管结构不那么简单。这是一个真正的极简设计，仅位于 CM4 的一个连接器上，仅暴露一个 UART、I2C 和 SPI。它需要带有板载大容量存储的 CM4 版本，但即使接口数量有限，它仍有很大潜力。

坚持极简主义，CM4 自身的外形为[Kamil Lorenc]的 uCM4、[提供了一个方便的模板，这是一个与 CM4 大小相同的主板，设计为一个小型网络发电站](https://hackaday.io/project/179793-ucm4)。当然，它有一个以太网端口，除此之外，还有一个用于电源和 USB2 的 micro USB，以及一个用于启动盘的 microSD 插槽。例如，有了 USB-OTG 支持，我们可以看到它变成一个从便携式设备也能访问的迷你网络。

当我们谈到网络外围设备时，有必要转向来自[mebs]的基于[CM4 的 NAS](https://hackaday.io/project/179338-cm4-custom-pcie-nas)。简单的 NAS 设备长期以来一直是 Raspberry Pi 的主打产品，这款设备将这一想法提升到了一个新的水平，PCIe 插槽支持 SATA 卡。这最终将基于 Pi 的 NAS 盒变成了可以与更传统的设备竞争的东西，因为虽然 Pi 3 上的 USB3 提供了速度，但它并没有提供太多的灵活性。

最后，在我们对 CM4 项目的快速总结中，是 StereoPi V2。我们之前提到过最初的 StereoPi，当我们看到第一块主板时，我们称赞它是一个演示，展示了如何使用早期的计算模块来构建自定义的 Raspberry Pi，而无需尝试购买 Broadcom 芯片。像原来一样，它包含了使 Pi 成为 Pi 的大多数接口，但它以自己的紧凑形式实现了这一点，并配备了两个摄像头连接器，这是它存在的理由。

我们希望有机会在一个地方看到所有这些 CM4 板会让你相信，把你自己从仅仅一个 Pi 的约束中解放出来是有意义的。我们希望 Raspberry Pi 的人们也能看到使用他们的作品所做的工作的广度，并使未来的计算模块变得更加容易访问。欢迎来到树莓派的新面孔！

标题图片:SparkFun， [CC BY 2.0](https://commons.wikimedia.org/wiki/File:CM_4_HERO_ON_WHITE_copy.jpg) 。