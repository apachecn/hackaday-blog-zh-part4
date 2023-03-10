# 带有 RasPi 改良游戏手柄的农业项目

> 原文：<https://hackaday.com/2019/04/02/farming-items-with-raspi-modified-joycons/>

这些年来，神奇宝贝游戏让众多任天堂游戏玩家欣喜不已，而且没有任何放缓的迹象。尽管它很受欢迎，但游戏的某些方面无疑是简单地通过努力获得成功。对[莫里·贝拉米]来说，这根本不行——然而他们对金瓶盖的渴望是无法满足的。怎么办？当然是自动化。

第一步是从任天堂 Switch 黑掉 Joycons。DG333A 模拟开关 IC 连接到内部的按钮，并由 Raspberry PI 的 GPIO 引脚控制。然后用 MCP4725 DAC 控制操纵杆，允许系统完全模拟控制台的控制输入。

现在控制台已经在树莓 Pi 的控制之下，下一步是增加智能。谷歌的 Tesseract OCR 平台结合了 Python 代码的帮助。这允许脚本从游戏中读取对话框，并使用这些数据来确定按下哪个按钮来农场物品。

[【Mori】已经将 GitHub 上的代码提供给他人使用](https://github.com/moribellamy/porygon/)，注意到稍加努力应该可以推广到其他游戏。从根本上说，底层硬件也可以很容易地重新用于其他控制器。有很多其他的方法来自动化游戏的苦差事，[即使你不得不使用触摸屏。](https://hackaday.com/2014/04/17/lego-robot-plays-games-for-you-as-you-sleep/)休息后的视频。

 [https://www.youtube.com/embed/JC_zD0W6a2I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/JC_zD0W6a2I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

