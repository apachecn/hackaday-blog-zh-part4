# 绕过 Wacom Cintiq Companion 2 上有缺陷的 STDP9320 视频控制器

> 原文：<https://hackaday.com/2023/01/04/bypass-defective-stdp9320-video-controller-on-wacom-cintiq-companion-2/>

有些产品似乎有两个部分，几乎肯定会死在你身上。就 2015 年的 Wacom Cintiq Companion 2 而言，这就是所谓的 Athena 芯片，它可以在 HDMI 端口和内部显示控制器之间切换显示输入。这允许在独立模式(平板电脑)和陪伴模式下使用，在陪伴模式下，它充当连接的 PC 的绘图板。当面对这样一个有缺陷的设备时，[【中微子】发现并应用了一个简单的修复方法](https://blog.project-insanity.org/2023/01/02/replacing-defective-bga-chip-with-wires/):完全绕过雅典娜芯片。

修复保护组织关于该主题的维基页面建议[进行此修复，指出这将永久禁止其用作外部显示器，而无需额外修复来重建被移除芯片的功能。ST 微电子公司的这款](https://repair.wiki/w/Wacom_Cintiq_Companion_2) [STDP9320](https://static6.arrow.com/aropdfconversion/8cc3fdfe16e31c1700aea8faac53e648e9ef1b73/dm00031849.pdf) (PDF)器件被描述为“带 3D 视频的优质高分辨率多媒体监视器控制器”，包含各种视频缩放器、HDMI 接收器、DisplayPort(包括嵌入式 DP)支持。通过这一修复，Cintiq Companion 2 的英特尔 CPU 图形核心直接连接到显示器的 eDP 输入，以及一系列电压和使能引脚。

STDP9320 在几年后死亡的确切原因似乎是某种内部电源故障或短路，但这种旁路修复至少恢复了独立功能。寻找这种过时 IC 的替代品似乎是可能的，但这是一场豪赌。可悲的是，这种 Wacom 设备似乎将不再是一个伴侣了。