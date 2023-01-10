# Dreamcast 现已推出无线 360 控制器

> 原文：<https://hackaday.com/2021/03/18/wireless-360-controllers-now-on-the-dreamcast/>

也许现代游戏机最大的便利功能是无线控制器。消除了被电线绊倒的风险，并支持在各种不符合人体工程学的位置上玩游戏，为主机游戏体验增添了巨大的舒适性。[伊斯梅尔]不喜欢 Dreamcast 的原始控制器，电缆太短，无法启动。是时候把 360 无线控制器带到世嘉的告别演出了。

[ismell]的早期尝试涉及一台 Windows 电脑作为 360 控制器的 USB 主机，然后通过 Cypress EZ-USB FX2 微控制器将命令发送回 Dreamcast。如果这听起来深奥和混乱，那是因为它是。它也太慢了，无法可靠地工作，因为 Dreamcast 的 Maple 控制器总线希望每毫秒更新一次，否则它会认为控制器断开连接。

相反，需要一个专用的 USB 主机来与 360 控制器和 Dreamcast 通信。[ismell]登陆 MicroZed 7010，这是一个片上系统，还在板上封装了一个 FPGA。随着 Petalinux 在板上运行，它与 Xbox 360 USB 无线控制器接口连接，然后通过自定义的“网络”驱动程序发送数据，该驱动程序通过 Maple 总线向 Dreamcast 发送数据包。

这绝不是一个简单的黑客，MicroZed 也不便宜，但它的工作和工作效果很好，如下面的视频所示。这些年来，我们也看到了其他无线控制器适配器，比如 wild BlueRetro build 。我们总是喜欢看到一个好的复古控制台黑客，[所以不要羞于发送你自己的！](http://hackaday.com/submit-a-tip)

[https://drive.google.com/file/d/1nLXLF5z0leBjxTOpl1LVw67GhCSi6-Zy/preview](https://drive.google.com/file/d/1nLXLF5z0leBjxTOpl1LVw67GhCSi6-Zy/preview)

