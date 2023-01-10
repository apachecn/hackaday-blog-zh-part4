# Macbook 借助仿 BGA PCB 获得 NVMe 固态硬盘

> 原文：<https://hackaday.com/2022/05/31/macbook-gets-nvme-ssd-with-help-of-a-bga-imitating-pcb/>

最近，我们偶然发现了[iBoff]的一个视频，为 2011-2013 年的 MacBook 添加了一个 M.2 NVMe 端口。苹果笔记本电脑从来没有合适的 M.2 端口，尤其是 a 1278——这是怎么回事？诀窍是——拆下一个 PCIe 连接的 Thunderbolt 控制器，然后在芯片所在的位置焊接一个类似 BGA 的插入器 PCB，并从那里将一个电缆组件拉到驱动器托架，那里有一个定制的适配器 PCB 在等待。该适配器甚至允许您将 PCIe 链接暴露为全尺寸的 PCIe 4x 插槽，以防您想要连接外部 GPU 而不是 NVMe SSD！

这个过程在视频中有很好的记录，作为任何试图安装这个特定 mod 的人的指导手册，也是任何有兴趣模仿它的人的见解和想法的集合。转接板附带有重新封装的焊球，因此它可以像 BGA 芯片一样安装，但电缆组件连接器不会安装在转接板上，因为它必须用热空气焊接到主板上，这样会熔化连接器。取代光驱的 PCB 也没有妥协，接入 SATA 连接器引脚，让您可以添加额外的 2.5 毫米 SATA SSD。

添加 NVMe 硬盘是一种不被看好的提高旧笔记本电脑速度的方式，因为它们都是引擎盖下的 PCIe，你可以通过添加它的特定方式来真正发挥创造力。你甚至不局限于替换像 Thunderbolt 控制器这样的不起眼的部件——如果一台笔记本电脑有一个独立的 GPU 和一个集成 CPU 的 GPU，你可以去掉独立的 GPU，用一个适配器代替一个，甚至两个 NVMe 驱动器，你所需要的只是一个与你的 GPU 占地面积相同的 PCB。遗憾的是，这个适配器的 PCB 文件似乎不是开源的，但是开发一个满足您自己需求的替代品最好从头开始，不管怎样。

我们以前见过这样的[为 Raspberry Pi 4](https://hackaday.com/2020/07/01/adding-pcie-to-your-raspberry-pi-4-the-easier-way/) 制作的适配器，可以代替 QFN USB 3.0 控制器芯片进行焊接，并将 PCIe 信号暴露在 USB 3 连接器引脚上。然而，这一个把它提高了一个档次！通常情况下，如果没有这样的适配器，我们必须[小心地焊接一根适当屏蔽的电缆](https://hackaday.com/2019/06/26/how-do-you-get-pci-e-on-the-atomic-pi-very-carefully/)，如果我们想从一个从未打算暴露的电路板上获得 PCIe 链接。PCIe 怎么了？为什么它很酷？我们[已经深入讨论过那个](https://hackaday.com/2021/02/03/the-bus-thats-not-a-bus-the-joys-of-hacking-pci-express/)！

 [https://www.youtube.com/embed/tvrygDOf0s8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/tvrygDOf0s8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

