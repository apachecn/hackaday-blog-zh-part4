# Amiga 现在通过 Raspberry Pi 子板提供 HDMI 接口

> 原文：<https://hackaday.com/2020/12/30/amiga-now-includes-hdmi-by-way-of-a-raspberry-pi-daughterboard/>

如果你在 16 位家用电脑时代有一台 Amiga，那么除了游戏和一点音频采样，你可能会选择它，因为它具有令人印象深刻的视频功能。在其全盛时期，Amiga 制作了广播质量的图形，甚至可以在 20 世纪 80 年代末和 90 年代初的许多电视节目中看到。公平地说，自从古鲁冥想的时代以来，电视世界已经发生了变化，SD 视频信号再也不能满足它了。随着 HDMI 成为当今的连接标准，【c0pperdragon】将通过[一种方便的 HDMI 升级](https://github.com/c0pperdragon/Amiga-Digital-Video)来提供帮助，它可以直接从 Amiga 的 Denise 芯片接入数字信号。

起初，人们可能会认为会涉及 FPGA，但实际上信号是通过子板输出到 Raspberry Pi Zero 的扩展头。只需移除 DENISE 显示编码器芯片，并使用长针脚机械 DIP 插座插入电路板进行连接。Pi 运行最初为 BBC Micro 设计的 [RGBtoHDMI](https://github.com/hoglet67/RGBtoHDMI) 项目中的软件，在 Pi 的 HDMI 输出上呈现 Amiga 图形的像素完美表示。需要说明的是，它运行在原始芯片组 Amiga 上，只有一些型号具有增强的芯片组，所以 Amiga 600 的所有者似乎被冷落了。据称延迟非常低，与解决相同问题的一些其他解决方案相比，这应该是有利的。

[这不是我们第一次看到 HDMI Amiga 转换](https://hackaday.com/2016/12/10/amiga-zorro-hdmi-graphics-card-hits-the-market/)，但它不仅仅适用于大型机器。

 [https://www.youtube.com/embed/ce9_zrPjY8U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ce9_zrPjY8U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

