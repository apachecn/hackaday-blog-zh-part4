# 将损坏的 PS4 控制器与替换的 PCB 连接

> 原文：<https://hackaday.com/2022/09/07/interfacing-broken-ps4-controllers-with-a-replacement-pcb/>

[Becky]有一些 PS4 控制器很遗憾不再起作用。然而，大部分的按钮和操纵杆看起来还是正常的。因此，她着手设计一个替代的 PCB，为这些以前用砖砌的游戏手柄注入新的生命。

在 PS4 控制器的情况下，大多数按钮都是薄膜类型的，通过柔性电缆上的一系列触点与主板内部进行对话。因此，[Becky]将她的 PCB 设计成可以读取大部分按钮。一个试验板和一个 LED 灯就派上了用场，可以计算出控制器上的哪个按钮对应哪个衬垫。替换操纵杆从亚马逊采购，直接焊接到替换 PCB 上。

[Becky]还利用 Fusion 360 的设计工具来 3D 打印最终设计的模拟图。这有助于在游戏手柄的外壳中找到合适的位置。

替换的 PCB 本身充当一个分支，以便游戏手柄的控制可以连接到微控制器。在这种情况下，控制器被重新用于运行循环音频项目的 RP2040 微控制器[。各种按钮和控制发射样本，允许简单的表演。](https://youtu.be/H3SuyhoAv2w?t=321)

那些渴望更换自己控制器的人可以自己制作控制器，Becky 已经在网上分享了设计文件。不过，如果你只是想以一种更少侵入的方式连接 PS4 控制器，[可以考虑这种替代技术](https://hackaday.com/2014/01/13/an-arduino-library-for-the-ps4/)。休息后的视频。

 [https://www.youtube.com/embed/H3SuyhoAv2w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/H3SuyhoAv2w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

