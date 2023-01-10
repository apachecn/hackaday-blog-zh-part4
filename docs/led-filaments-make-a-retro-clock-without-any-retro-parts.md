# LED 灯丝制造了一个没有任何复古零件的复古时钟

> 原文：<https://hackaday.com/2022/04/05/led-filaments-make-a-retro-clock-without-any-retro-parts/>

我们喜欢 Hackaday 的时钟项目，我们已经看到了许多基于各种显示技术的美丽设计。有各种类型的玻璃管，如 Nixies，Numitrons 和经典的 VFD 显示器，所有这些都有温暖的“复古”光芒。然后是发光二极管，这对于制造基于像素的酷酷的计时器很有用，并且易于用低压电子设备驱动。那么，如何结合两个世界的优点，通过使用 led 来制作一个类似纳米晶体管的显示器呢？这正是杰伊·哈姆林(Jay Hamlin)在基于 LED 灯丝(T1)制造数字时钟(T0)时所做的。

该项目的核心由橙色 LED 灯丝组成，类似于老式 LED 灯泡中使用的灯丝。[Jay]在网上买了一堆，并尝试了各种方法将它们组合成七段显示器，最终选择了一个黑色的小 PCB，以便在 led 和背景之间形成良好的对比。为了让显示器看起来像是被玻璃包裹着，[杰伊]买了一套塑料试管，并将其切割成合适的尺寸。

时钟的底座由一个光滑的黑色 PCB 构成，PCB 上有一个 ESP32。这些段通过一组 74LV595 移位寄存器驱动，以保持所需的 GPIOs 数量最少。没有按钮:由于 WiFi 连接和网络时间协议，ESP32 自动保持正确的时间。

最终结果乍一看非常像一个 Numitron 显示器，即使你注意到没有玻璃，它仍然是一个制作精美的时钟。如果你喜欢 LED 灯丝时钟(谁不喜欢呢？)，看看[这个模拟挂钟](https://hackaday.com/2021/06/25/a-custom-clock-with-led-filament-hands/)，或者[这个蜘蛛网一样的数字钟](https://hackaday.com/2018/08/01/old-led-light-bulbs-give-up-filaments-for-spider-web-clock/)。

 [https://www.youtube.com/embed/gkYBQIplHyQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/gkYBQIplHyQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

