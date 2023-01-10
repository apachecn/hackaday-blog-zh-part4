# 手表上链器让你的钟表走得更快

> 原文：<https://hackaday.com/2020/09/06/watch-winder-keeps-your-timepieces-ticking/>

机械表是微小工程的胜利。能够通过捕捉用户自身运动的能量来计时，它们从来不需要更换电池。不幸的是，几天不穿，它们很快就会失去时间。为了解决这个问题，[sblantipodi] [造了一个智能手表上链器](https://github.com/sblantipodi/smart_watch_winder)。

整个建筑由六个独立的收卷机单元组成。每个都有一个 ESP8266EX D1 微型微控制器，连接到一个 28BYJ48 步进电机和一个 ULN2003 电机驱动器。还有一个显示状态信息的有机发光二极管屏幕。收到指令后，步进电机转动，转动表壳，为钟表上弦。由于谷歌 Home Mini 和 Raspberry Pi 运行家庭助手，控制是通过语音命令进行的。手表可以单独上弦，也可以一起上弦，这取决于给定的指令。

这种装置可以很好地服务于任何收藏家，并且可以方便制表商为等待提货的顾客手表上弦。其他类似的产品使用了特殊的静音驱动器，以确保该设备在床头柜上使用时不会打扰睡眠。休息后的视频。

 [https://www.youtube.com/embed/4MUGdeRXrfY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/4MUGdeRXrfY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

