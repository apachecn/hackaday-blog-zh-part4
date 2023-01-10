# 用自制的便携式烙铁加热包装

> 原文：<https://hackaday.com/2021/08/17/packing-heat-with-a-homemade-portable-soldering-iron/>

小型便携式烙铁风靡一时，所以[电子人]决定自己制造一个。虽然这种设计不像商用设备那么时尚，但考虑到它自带电池，它看起来相当不错。

当然，问题是:有效吗？你可以在下面的视频中看到，它可以在大约十秒钟内熔化焊料。重量在 100 g 左右，用起来应该很舒服。

一个小显示屏显示操作参数。我们还喜欢吸头的螺纹支架。尖端需要来自电池的大约 4 A，这导致 15 W 熨斗。然而，吸头没有内置热电偶，因此您无法精确控制吸头的温度。

欠压检测有一点问题，所以如果电压降得太低，您需要准备好手动移除电池。这有点痛苦，我们可能会考虑连接一个物理电源开关，以避免过于频繁地打开 3D 打印的外壳。

PCB 上有一个 Arduino、一个 MOSFET 和一些用于监控电池电流和尖端电阻的仪器。当然，你可以对固件做任何你想做的事情，进行任意数量的定制。

虽然这款熨斗看起来有点像 TS-100，但它不包含电池，所以你必须携带外部电源或电池。但是有[带电池的商用熨斗](https://hackaday.com/2017/09/12/hakko-fx-901-better-than-ts-100/)。当然，已经有[其他类似的项目](https://hackaday.com/2016/07/26/ugly-diy-portable-soldering-iron/)，但我们喜欢这个的外观和可扩展性。

 [https://www.youtube.com/embed/sK0Mkh3s-Mw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/sK0Mkh3s-Mw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

