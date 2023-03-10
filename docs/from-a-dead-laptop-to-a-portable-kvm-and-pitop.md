# 从废弃的笔记本电脑到便携式 KVM 和 PiTop

> 原文：<https://hackaday.com/2019/03/10/from-a-dead-laptop-to-a-portable-kvm-and-pitop/>

许多系统管理员的一个基本工具是一个便携式终端，可以随时插入一个出现故障的机架式服务器来进行急救。在最简单的情况下，它们只是手推车上的显示器和键盘，但更多情况下，它们是预装了工具的笔记本电脑。系统管理员将顽强地坚持使用现在这种应用程序的老式笔记本电脑，因为它们拥有一个硬件串口。

[弗兰克·亚当斯]用他的紧急服务器急救车走了一条不同的路，因为虽然他使用的是旧笔记本电脑，但他没有保留它的原始硬件。相反，他用一块 Teensy 和一块 LVDS 驱动板替换了两台旧的戴尔 Latitude 笔记本电脑的主板，其中一台是简单的 KVM 设备，另一台是自带 Raspberry Pi 3 的笔记本电脑。他还制作了一个视频，我们把它放在休息时间的下面。

曾经有一段时间，笔记本电脑显示屏被认为是不可拆卸的，但廉价驱动板的出现意味着像这样的转换已经成为一种相对陈旧的方式。不过，他在这里的工作做得特别好，很好地利用了老式企业级笔记本电脑中的大量空间。没有电池，因为这种应用不需要电池，但是，在电池盒完好无损的情况下，可以包括合适的充电器/监控板以及升压转换器，以提供 12V 电源。

这不是我们看到的第一台在重复使用的商用机器中的 Pi 笔记本电脑，还有这台索尼 Vaio。

 [https://www.youtube.com/embed/M5-dYo2jt14?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/M5-dYo2jt14?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



谢谢[莫里斯]的提示。