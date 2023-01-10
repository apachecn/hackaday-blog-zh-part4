# 这是厄运，这一次在蓝牙 LE Dongle

> 原文：<https://hackaday.com/2021/11/20/its-doom-this-time-on-a-bluetooth-le-dongle/>

到目前为止，大多数读者应该已经习惯了这样一种现象，即拿起几乎任何一个微控制器，哄它运行 20 世纪 90 年代所有第一人称射击游戏的始祖，id Software 的 *Doom* 。它已经在各种设备上完成，有时只有足够的电力用于演示模式，但更多时候能够提供完整的体验。在这个像素化戈尔的节日中，最新的滑门是【尼古拉·拉钦】，他的[使用基于 nRF52840 的 USB 蓝牙电子狗](https://hackaday.io/project/181224-doom-on-an-nrf52840-based-usb-bluetooth-dongle)实现了这一壮举。

完整的细节可以在他的网站上找到[，那里详细介绍了使用 Adafruit 线索板进行初始开发的过程。一个 16MB 的闪存芯片用于 WAD 存储，一个 SPI 彩色显示器将我们直接带到火卫一上那个被诅咒的基地。目标板缺少足够的 I/O 来连接到屏幕和闪存，因此需要一些 7400 逻辑的诡计来为任务释放足够的空间。使用 nRFS1822 板，通过无线游戏手柄实现控制，并将音频流传输到 PWM 输出。](https://next-hack.com/index.php/2021/11/13/porting-doom-to-an-nrf52840-based-usb-bluetooth-le-dongle/)

结果可以在休息时间下面的视频中看到，它显示了一个非常可玩的游戏，既有*毁灭战士*又有*毁灭战士 2* ，这不会让那个时代的许多机器蒙羞。这是一个 Adafruit 线索板上的原型，这可能是你一直在寻找的手持控制台！

 [https://www.youtube.com/embed/kUsfgSCRpG0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/kUsfgSCRpG0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

