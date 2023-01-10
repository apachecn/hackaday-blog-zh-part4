# 将可穿戴显示器切成两半比看起来更难也更简单

> 原文：<https://hackaday.com/2022/10/16/cutting-a-wearable-display-in-half-is-harder-and-simpler-than-it-seems/>

在硬件黑客的世界里，你有时会花大量的时间调试一个问题，却发现一个简单的解决方案一直就在你面前。[扎克·弗里德曼]在制作[Optigon V2](https://www.youtube.com/watch?v=77hET4FhH_0)时很好地体验了这一点，这是一款经过改装的爱普生 Moverio 可穿戴显示器，他在所有视频中将其用作提词器。他更喜欢只在左眼上安装提词器，但新版 Moverio 会在其中一个断开时关闭两侧，所以[Zack]需要一个变通办法。

[Zack]向上面寻求帮助，要求 Epson 提供显示器模块的开发人员文档，但被拒绝了，因为他不是制造商或产品开发人员。幸运的是，可以从爱普生网站下载的规格表确实包含了很多他需要的信息。STM32 通过一对独立的 I2C 接口监控每个显示模块的温度，如果无法连接到任何一个接口，就会关闭所有设备。这导致[Zack]试图用 ATmega328 伪造 I2C 信号，但它跟不上 400 kHz 的 I2C 总线。

然而，查看他的逻辑分析仪的日志，[Zack]发现 STM32 从未同时与两个显示模块对话，尽管它能够这样做。两个显示器使用相同的 I2C 地址，所以[Zack]可以简单地用一个简单的接口板将两条 I2C 总线相互连接起来，有效地使左显示器“欺骗”右显示器的信号。

可穿戴显示器需要一些奇特的光学器件才能实用，[你不能只是把有机发光二极管贴在脸上](https://hackaday.com/2021/08/19/why-you-cant-make-build-a-wearable-display-with-a-just-a-transparent-oled/)。扎克的另外两个有趣的项目是他的[模块化机械键盘](https://hackaday.com/2022/08/02/the-rollercoaster-of-developing-the-ultimate-hackable-keyboard/)和 [Gridfinity 3D 打印存储系统](https://hackaday.com/2022/04/18/gridfinity-3d-printed-super-quick-tool-storage-and-retrieval/)。

 [https://www.youtube.com/embed/77hET4FhH_0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/77hET4FhH_0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

