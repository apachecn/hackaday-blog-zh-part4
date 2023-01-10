# 在选定的 Arduino 板上拖放文件

> 原文：<https://hackaday.com/2019/05/29/drag-and-drop-files-on-select-arduino-boards/>

从历史上看，把文件放到微控制器设备上是一个麻烦的过程。您可能会发现自己需要手动将图像数据放入代码中的数组中，或者反复换入换出 SD 卡。对于特定的 Arduino 板，这不再是一个问题—[感谢 Adafruit 的新 TinyUSB 库(Youtube 链接，嵌入在下面)](https://www.youtube.com/watch?v=0bWba0PU4-g)。

[该库在 Github](https://github.com/adafruit/Adafruit_TinyUSB_Arduino) 上可用，兼容 SAMD21 和 SAMD51 板，以及 Nordic 的 NRF52840。它允许 Arduino 板看起来像一个 USB 驱动器，文件可以简单地拖放到位。该库可以设置为使用 SPI 闪存、SD 卡甚至内部芯片存储器作为存储介质。

潜在的应用包括图像、音频文件、字体甚至配置文件。未来的计划还包括将 TinyUSB 库移植到 ESP32-S2。能够将设置文件直接拖到主板上可以让 WiFi 主板上网变得不那么麻烦。

我们以前见过其他漂亮的 USB 库，如果你的 AVR 微控制器需要 USB，VUSB 是一个很好的选择。休息后的视频。

 [https://www.youtube.com/embed/0bWba0PU4-g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/0bWba0PU4-g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

