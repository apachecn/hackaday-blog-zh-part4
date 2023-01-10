# 用于复古计算机的现代网络适配器

> 原文：<https://hackaday.com/2020/10/14/modern-network-adapter-for-retro/>

通用串行总线(USB)在现代计算中根深蒂固，很难想象没有它的时代。然而，那个时代确实存在，它是连接器类型、标准和接口方法的蛮荒之地。当时更有趣的接口之一是 8 位 Atari 计算机中的 SIO 系统，该系统最终共享了现代 USB 的许多功能，其适应性在[这个现代项目中得到了展示，该项目将 WiFi、蓝牙、USB 和 SD 卡插槽引入任何带有 SIO 端口的旧 Atari](https://github.com/FujiNetWIFI/fujinet-platformio/)。

该项目名为 [FujiNet](https://fujinet.online/) ，它使用 SIO 的轻量级协议为 8 位机器添加了许多现代功能。它基于 ESP32，该芯片通过将 WiFi 和蓝牙连接到 Atari 来执行网络适配器的功能。它通过模拟 Atari 当时可能使用的驱动器，如软盘驱动器、RS232 接口或调制解调器，并将它们转换为现代无线通信协议来实现这一点。它甚至能够通过从 Atari 获取打印作业的输出并在设备本身内将其转换为 PDF 来模拟打印机。

这不仅给雅达利带来了很多功能，你可以用它来浏览像[retro.hackaday.com](http://retro.hackaday.com/)这样的网站，而且 FujiNet 被装在一个与时代相适应的 3D 打印的盒子里，与最初的雅达利的外观和感觉相匹配。如果你需要一个更通用的解决方案来进行你的逆向计算网络冒险，而不局限于 SIO，我们[推荐你用树莓 Pi 来处理这个](https://hackaday.com/2020/06/01/easy-internet-for-retro-computers-with-the-pimodem/)。

感谢[加文]的提示！