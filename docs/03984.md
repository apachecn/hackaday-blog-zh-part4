# OTA Flash 工具让健身追踪器黑客攻击变得更加容易

> 原文：<https://hackaday.com/2019/08/23/ota-flash-tool-makes-fitness-tracker-hacking-more-accessible/>

在过去的几个月里，[Aaron Christophel]一直致力于为廉价的健身追踪器创建一个定制的固件。他目前的目标是来自 MPOW 公司的“D6 追踪器”,售价仅为 7 美元。最终目标是让任何人都能够使用 Arduino IDE 为这个小工具编写自己的定制固件，随着他的新 Android 应用程序[的发布，该应用程序允许无线刷新设备的固件](https://play.google.com/store/apps/details?id=com.atcnetz.ble.readwrite)，他似乎非常接近实现这个梦想。

以前，[Aaron]必须打开追踪器并物理连接一个程序员来更新基于 NRF52832 的设备上的固件。对于有经验的硬件黑客来说，这可能没什么大不了的，但是对于那些只想看到自己的 Arduino 代码在上面运行的人来说，这就有点难以接受了。但有了这个新工具，他已经做到了，所以你可以轻松地在 D6 上的定制和原始固件之间来回切换，甚至不必从手腕上取下它。

休息过后，你可以看到[Aaron]整理的视频，它讲述了刷新新固件映像的过程。这非常简单:您只需从检测到的 BLE 设备列表中选择设备，应用程序将跟踪器置于引导模式，然后选择您想要刷新的 DFU 文件。

现在有一些现成的固件你可以放在 D6 上，但是这有什么意思呢？[Aaron]已经组装了一个 Arduino IDE 的定制版本，它提供了开始编写和刷新您自己的固件所需的一切。如果你曾经梦想过创造一个完全按照你想要的方式工作的可穿戴设备，很难想象有更便宜或更容易的方式来参与其中。

[今年早些时候](https://hackaday.com/2019/02/20/custom-firmware-for-cheap-fitness-trackers/)我们最后一次听到【Aaron】的消息时，他正在开发 IWOWN I6HRC 追踪器。但是看起来这些设备的可用性已经枯竭了。因此，如果你打算尝试破解 MPOW D6，趁它们还便宜且容易找到，现在买几个可能是明智的。

 [https://www.youtube.com/embed/3gjmEdEDJ5A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/3gjmEdEDJ5A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

