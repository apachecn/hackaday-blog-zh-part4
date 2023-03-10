# ESP32-S2 样品出现

> 原文：<https://hackaday.com/2020/03/23/esp32-s2-samples-show-up/>

ESP8266 现在已经有六年的历史了，而 ESP32 也日益成为主流。不出所料，Espressif 正在开发更新的产品，ESP32-S2 去年就在一些测试人员手中。现在它终于作为“最终硅”样品降落在人们手中。[意想不到的制造者]得到了一些芯片的原型开发板，[在最近的视频中分享了他的发现。](https://www.youtube.com/watch?v=F1GOSsNZCRg&feature=emb_logo)

ESP32-S2 有一个运行在 240 MHz 的单核 LX7 和一个基于 RISC-V 的协处理器。板载是 320K 的 RAM 和 128K 的 ROM。你可能会注意到它比 ESP32 小。然而，该设备可以支持高达 128MB 的外部 RAM 和高达 1GB 的外部闪存。它还支持 USB，尽管原型模块似乎有一个外部 USB 芯片。

没有蓝牙、以太网或 CAN 之类的额外功能，但有 43 个 GPIO 和 14 个触摸传感器。还有其他的不同，有正有负。有两个 UARTs，低于 ESP32 的三个。然而，还有一个摄像头接口和更多的加密硬件。有一种方法可以使用 WiFi 的飞行时间测量来估计位置，如果效果好的话，这可能会很有趣。

不过，大新闻是自动电源管理，它声称在空闲模式下为 5uA，在 1%占空比下为 24uA(运行 ULP 协处理器时)。老实说，看起来 S2 更像是一个安全的 ESP8266，而不是下一代的 ESP32。这并不完全公平，因为新板的处理能力比 ESP8266 强得多，但仍然如此。

当埃斯普雷西夫宣布这个消息时，我们看着 S2。ESP-32 可以[在相对较低的功率下工作](https://hackaday.com/2020/01/07/how-low-can-an-esp32-go/)，但是——S2 应该可以使更低的功率操作更加容易。

 [https://www.youtube.com/embed/F1GOSsNZCRg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/F1GOSsNZCRg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

