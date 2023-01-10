# 最好的笔记本电脑变得更好

> 原文：<https://hackaday.com/2018/11/24/the-best-laptop-gets-even-better/>

ThinkPad 是有史以来最伟大的笔记本电脑。它没有玫瑰金，只有黑色。它没有一个奇怪的屏幕，而是一个退出键。不到 MacBook 一半的价格，你就可以拥有一台内置三个硬盘的笔记本电脑。这很疯狂，但它仍然不是黑客攻击的完美工具。要实现这一点，你需要用一个独立的 Linux 系统来装载它，也许还需要一个无焊试验板。这就是[ollie242]正在用他的 ThinkPad 做的事情，其结果是对完美笔记本电脑的完美补充。

这种构建实际上只是用于 [Thinkpad UltraBay](https://en.wikipedia.org/wiki/ThinkPad_UltraBay) 的 3D 打印驱动器盒，这种模块化标准允许您为笔记本电脑添加 CD 驱动器、SATA 驱动器，甚至是串行和并行端口。[ollie242]正在模仿从 ThinkPad T420 上取下的 CD 驱动器，因此我们正在寻找这一标准的“串行 Ultrabay 增强”版本，它与 T430 兼容，T430 仍然是你可能买到的最好的笔记本电脑。

在这个 3D 打印的驱动器盒中有一个 Raspberry Pi Zero W，由 ThinkPad 通过内部 SATA 连接器供电。Pi Zero 附有直角接头，可以从外部访问 GPIO 引脚。为了增加一点趣味，[ollie242]添加了一个有机发光二极管显示器来显示 Pi 的 IP 地址、CPU 负载和内存可用性。

这是一个伟大的项目，如果只是因为没有人有任何使用光盘驱动器了。由于这些 UltraBay 驱动器非常庞大，因此向驱动器添加一台更强大的计算机[将是一件简单的事情，就像最近发布的 Raspberry Pi 3 型号 A+](https://hackaday.com/2018/11/15/the-smaller-more-powerful-raspberry-pi-3-model-a/) 。在 UltraBay 端口上有——或者至少应该有——一些有趣的内部连接，不难想象这个 Raspberry Pi UltraBay 可以用作其主机笔记本电脑的某种协处理器。