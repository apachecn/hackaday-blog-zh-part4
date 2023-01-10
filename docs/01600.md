# FPGA 模拟 PDP-1，为经典视频游戏注入新的活力

> 原文：<https://hackaday.com/2018/12/21/fpga-emulates-a-pdp-1-breathes-new-life-into-classic-video-game/>

如果你曾经想坐在开启交互式计算革命的机器的控制台前，你的选择是极其有限的。在数字设备公司制造的 53 台 PDP-1 机器中，已知只有三台仍然存在，并且只有一台机器仍然在计算机历史博物馆中正常工作。如此激动人心的太空战游戏！原始硬件上的东西可能不是你的遗愿清单上的东西。

但是多亏了[Hrvoje]，现在有了 PDP-1 的 FPGA 模拟，让你不用进入 CHM 就能玩所有视频游戏的鼻祖。这个项目开始只是为了给[Hrvoje]一个学习 FPGAs 和 Verilog 的沙盒，但显然不止于此。该仿真具有完整的 PDP-1 指令集、4kB 的核心存储器以及原始纸带阅读器、电传打字机、操作员控制台和经典 30 型 CRT 的表示。所有的硬件都显示在一个标准的 HDMI 显示器上，但真正起作用的是 CRT 实现。最初的 30 型显示器使用的是雷达设备中的阴极射线管，并且具有长余辉磷光体，使显示器具有非常独特的外观。[Hrvoje]通过将每个像素作为三个值(X、Y 和亮度)存储在一个由四个链式移位寄存器组成的循环中，复制了这一点。当像素通过移位寄存器时，亮度值降低，因此慢慢变暗。[Hrvoje]认为这看起来不太对，但我们会恭敬地不同意这一点。

我们之前已经争论过，PDP-1 是开创黑客文化的机器，我们认为这个项目是对机器的恰当致敬，因为我们进入了它将迎来 60 岁生日的一年。通过这次竞赛有机会和它一起玩简直是为它的生日蛋糕锦上添花。

 [https://www.youtube.com/embed/iymD9eysqXo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/iymD9eysqXo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

