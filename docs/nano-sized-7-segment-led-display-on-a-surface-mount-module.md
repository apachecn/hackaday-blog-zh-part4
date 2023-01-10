# 表面贴装模块上的纳米级 7 段 LED 显示屏

> 原文：<https://hackaday.com/2022/11/30/nano-sized-7-segment-led-display-on-a-surface-mount-module/>

受一条恶作剧推特的启发，[Sam Ettinger]努力创造一个 SMD 七段展示。 [NanoRaptor NanoSegment](https://hackaday.io/project/188395-the-nanoraptor-nanosegment/) 实现了一个七段显示模块面板，每个模块尺寸为“0806 ”,比标准 0805 SMD 尺寸略宽。七段中的每一段都是一个 0201 LED。操作每个模块需要六条 I/O 线和三个电阻。

为了演示他的微型显示模块的操作，Sam 还创建了“6 pin 7 seg”[开发板](https://github.com/settinger/nanoraptor_nanosegment/tree/main/kicad)，该开发板具有 ATtiny84 微控制器，该微控制器与 PCB 尺寸相耦合，以容纳 NanoRaptor NanoSegment 显示模块。通过显示在一个微小的七段模块上的数字来演示电路板计数。

希望将模块的接口减少到两个引脚，Sam 现在正在试验一种柔性 PCB 上的七段显示器，这种显示器可以折叠成 1208 尺寸。他正试图将电阻和 ATtiny20 微控制器折叠成一个“折纸 PCB”结构。

如果这些内容对你的口味来说有点太小，我们为你准备了这个[巨型七段显示器](https://hackaday.com/2022/07/27/you-can-build-a-giant-7-segment-display-of-your-very-own/)。