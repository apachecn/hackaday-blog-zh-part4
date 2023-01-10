# 一对时尚的 FPGA 耳环

> 原文：<https://hackaday.com/2019/05/24/a-stylish-pair-of-fpga-earrings/>

有时候，与其走商业化路线，不如为这种个人风格制作一份礼物。[Mahesh Venkitachalam]以前也走过这条路，经常被这个常见的障碍绊倒:陷得太深，完全错过了这个场合的最后期限。不想重蹈覆辙，帮助很早就被征募了，[于是冰珍珠耳环诞生了。](https://electronut.in/ice-bling-making-led-earrings-with-an-fpga/)

这对耳环是送给[Mahesh]妻子的礼物，是和帮忙设计的朋友合作制作的。耳环使用晶格 iCE40UP5k FPGA 来控制 8×8 网格的 SMD LEDs。所有这些都是在不使用移位寄存器的情况下实现的，led 全部由 GPIO 引脚直接驱动。这带来了一些挑战，例如布线所有连接和向 led 提供足够的电流。最终的 PCB 是 4 层设计，这使得所有线路更容易有效布线。缓冲器用于避免同时运行太多 led 损坏 FPGA。

这是一个整洁的构建，它对元件放置和 PCB 设计做出了明智的选择，以产生一个有吸引力的最终结果。led 很自然地适用于珠宝应用，这些年来我们已经看到了一些很棒的设计。休息后的视频。

 [https://www.youtube.com/embed/EQmQjjXrsqI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/EQmQjjXrsqI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

