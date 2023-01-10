# RISC-V 上的 NES

> 原文：<https://hackaday.com/2019/03/14/nes-on-risc-v/>

RISC 架构可能会改变世界，但它现在运行的是 NES 仿真器。[这要感谢 MaixPy](https://github.com/sipeed/MaixPy) ，K210 的新 MicroPython，最近发布的 RISC-V 微控制器在社区中掀起了波澜。[【机器人零一】有教程](https://robotzero.one/micropython-nes-emulator-on-a-risc-v-64-processor/)，EEVBlog 的【其他戴夫】有[的视频](https://www.youtube.com/watch?v=el6CB-h9Lo0)。

Sipeed K210 去年 10 月在淘宝上以一种奇怪的预购形式来到英语世界承诺双核 RISC-V CPU 仅售几美元。Seeed，将 ESP8266 投入大规模销售的同一批人很快跟上潮流，[于去年 2 月](https://hackaday.com/2019/02/14/new-part-day-a-risc-v-cpu-for-eight-dollars/)开始销售模块。现在，Seeed 正在研究使用 Sipeed 模块的[树莓派帽子](https://forum.seeedstudio.com/viewtopic.php?f=110&t=31497&p=52523&fbclid=IwAR1V2pGtGF0Uf92_la4M1n92C3JSdE6wQ5nCY8j5k6ZNTAECepGOMYelKX4#p52523)，RISC-V 微控制器的未来看起来很棒。现在有人只需要写一些软件。这正是 Sipeed 的工程师们所做的，在其中一个发布的二进制文件中有一个 NES 模拟器。

类似于某个东西是否可以运行 Doom 的问题是，某个东西是否可以运行 NES 仿真器，所以随着对 K210 的 MicroPython 支持的发布，显而易见的事情就是发布 NES 仿真器。所需的硬件是 Maix M1w Dock，可从 [Seeed](https://www.seeedstudio.com/Sipeed-M1w-dock-suit-M1w-dock-2-4-inch-LCD-OV2640-K210-Dev-Board-1st-RV64-AI-board-for-Edge-Computing-p-3207.html) 和 [Banggood](https://www.banggood.com/Sipeed-M1-W-Dock-Development-Board-with-WIFI-2_4-inch-320240-LCD-Screen-OV2640-Camera-Kit-p-1410624.html?cur_warehouse=CN) 获得。

对 MicroPython 的新支持很棒，NES 仿真器也很棒，但这并不奇怪。[从两年前我们第一次接触到第一个开源微控制器](https://hackaday.com/2017/01/05/hands-on-with-the-first-open-source-microcontroller/)开始，RISC-V 显然更快。现在它很便宜，我们迫不及待地想知道接下来会发生什么。

 [https://www.youtube.com/embed/el6CB-h9Lo0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/el6CB-h9Lo0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

