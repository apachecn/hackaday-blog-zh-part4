# 运行微型 PDP11 的微型 VT102

> 原文：<https://hackaday.com/2021/01/18/a-miniature-vt102-running-a-miniature-pdp11/>

我们花了很多时间来研究游戏和家用计算机形式的逆向计算，但确实可以说小型机没有硬件项目那么普遍。也许是原始机器的大小、成本，甚至相对稀有，但 DEC 小型计算机在这里有点不寻常。[Sprite_TM]没有为我们购买 PDP11 或 VT102 终端，但他做了一件退而求其次的事情，即[一个微型工作 VT102，它还隐藏了一个 PDE11 仿真器](https://spritesmods.com/?art=minipdp11&page=1)。它运行俄罗斯方块和 2.1BSD 操作系统，俄罗斯方块最初是在 PDP11 架构的俄罗斯克隆版上开发的。

驱动这一切的是 ESP32 模块，PDP11 仿真器是著名的 SIMH 软件。将它移植到微控制器稍微受限的环境需要一些妥协，即网络堆栈和配置接口。[Sprite_TM]通过编写一个通过 SIMD 直接从 BSD 获取网络数据包的 ESP32 层，实现了 BSD 联网。它包括自己的 DHCP 客户端和无线网络配置工具，允许一个源自 20 世纪 70 年代的古老 UNIX 操作系统通过一个去掉网络代码的仿真器连接到 21 世纪的互联网。

该案例是 OpenSCAD 中的杰作，这是一个完整的 VT102 微型装置，带有一个微型 LCD 屏幕，当在树脂打印机上打印时，它是真实事物的非凡复制品。它没有键盘，但即使有一个微型蓝牙板，它看起来仍然令人印象深刻。在休息时间下面的视频中，他将其引导至 2.1BSD，重要的是，因为这是一个服务器操作系统，他从笔记本电脑登录并玩了一个 *Zork* 游戏。

这些年来，[Sprite_TM]使用 ESP32 和其他器件为我们带来了许多令人印象深刻的项目。也许你有一个最喜欢的，但对我们来说是[像 PocketSprite 游戏机一样的小型掌上游戏机](https://hackaday.com/2018/02/12/hands-on-with-the-smallest-game-boy-ever-made/)。

 [https://www.youtube.com/embed/jtmNOZVrz98?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/jtmNOZVrz98?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

