# 从残破的联想 Yoga Book 中抢救 Wacom 数字化仪

> 原文：<https://hackaday.com/2021/09/23/rescuing-a-wacom-digitizer-from-a-broken-lenovo-yoga-book/>

联想 Yoga Book 是一个有趣的东西，它有一个触摸屏键盘，还可以兼作 Wacom 平板电脑。[TinLethax]在尝试更换 Yoga Book 中的电池时，不幸打碎了键盘的玻璃，但发现 Wacom 数字化仪仍然完好无损。因此开始了一个项目来挽救这一部分，并将其重新用于未来。

第一步是对硬件进行逆向工程；事实证明，数字化仪板连接到一个特殊的 Wacom W9013 芯片，该芯片保存了该公司的秘密酱(秘密烟雾？).然而，正如[TinLethax]的 [WacomRipoff 驱动程序](https://github.com/TiNredmc/WacomRipoff)的 GitHub 页面所解释的，该芯片通过 I2C 进行通信。因此，连接一个微控制器(本例中是 STM32 器件)并向主机发送 USB HID 数据是一件非常简单的工作。

它并不是一帆风顺的，也不是 100%的功能完整，但[TinLethax]能够让数字化仪作为 USB HID 输入设备工作。看起来按钮和压力敏感度也很正常。

如果你有一本废弃不用的瑜伽书，你可能也会考虑同样的方法。我们在这个领域也看到了一些其他优秀的黑客。休息后的视频。

 [https://www.youtube.com/embed/DsoRSscmnTo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/DsoRSscmnTo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

