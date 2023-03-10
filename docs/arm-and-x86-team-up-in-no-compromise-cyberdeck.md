# ARM 和 X86 在毫不妥协的网络平台上合作

> 原文：<https://hackaday.com/2020/12/05/arm-and-x86-team-up-in-no-compromise-cyberdeck/>

在过去的几年里，网络社区绝对是爆炸式增长。在那些设计和制造这些真正的个人电脑的人当中，没有硬性的规则，除了确保最终的结果看起来尽可能的不传统。但有一件事保持相当一致，那就是这些机器几乎完全由树莓派驱动。不幸的是，这意味着他们经常在原始性能方面有所欠缺。

但是[MSG]有不同的想法。[他的 cyberdeck 内部仍然有惯常的 Raspberry Pi](https://msglab.co/room/msg-background)，但它也有一个 i7 英特尔 NUC，只需按一下按钮就可以启动。他说这是两个世界中最好的:一个高能效的 ARM Linux 平台用于移动实验，一个强大的 x86 Windows box 用于在家工作的 T2 玩游戏。这就像黑客一样，生意在前，聚会在后。

[![](img/06ab4a61666a123c40225e8b6523e025.png)](https://hackaday.com/wp-content/uploads/2020/11/msg_detail.jpg) 用一个 KVM 连接到定制的 Planck 40%机械键盘和七英寸 LCD，【MSG】可以在两个系统之间动态切换。假设他有足够的精力。虽然 Raspberry Pi 4 和 LCD 可以使用一对 18650 电池，但如果他想使用耗电的 NUC，则需要插入 cyberdeck。如果他放弃了 Pi，他可能会在机箱中装入足够的电池来启动英特尔盒子，但这将有点太接近传统的笔记本电脑。

整个多元化主题也不仅仅停留在计算设备上。除了主 LCD，还有一个 2.13 英寸的电子纸显示器和一个复古风格的 LED 矩阵，由 Pimoroni Micro Dot pHAT 提供。通过幕后的一点 Python 魔术，[MSG]能够显示诸如系统温度、时间和电池百分比之类的东西，即使在 LCD 关闭时也是如此。

[在名副其实的 *Cyberdeck Cafe* 上的一篇帖子中，【MSG】](https://cyberdeck.cafe/mix/msg)谈到了[是如何看到由【bootdsc】建造的 VirtuScope 的，这激发了他](https://hackaday.com/2019/09/20/3d-printed-virtuscope-is-a-raspberry-pi-4-cyberdeck-with-a-purpose/)开始致力于他自己的个人甲板，以及他希望从这里把这个想法带到哪里。屏幕后面独特的 USB 扩展舱具有特殊的前景，听起来好像一些附加模块已经在工作中。但是，当然，如果不是不断地被改进和重新设计，它就不是一个真正的赛博甲板。仔细想想，在这个社区里至少有两条生活准则。