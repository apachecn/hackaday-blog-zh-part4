# 这款 LED 空气传感器项链让您轻松呼吸

> 原文：<https://hackaday.com/2022/03/23/breathe-easy-with-this-led-air-sensor-necklace/>

当你在制作可穿戴设备和 glowables 时，有时一个华丽的彩虹动画就足够了。[极客 Faye]喜欢走得更远一点，然而，他制作了这条令人印象深刻的项链[,用来告知当地的空气质量。](https://github.com/geekyfayeart/Clean-Air-Necklace)

这款项链由一系列 Neopixel LED 灯条组成，安装在由柔性细丝制成的整洁的 3D 打印外壳中。燕尾榫使得戴上和取下项链变得轻而易举。一个基于 ESP32 的 TinyPico V2 主持了这场表演，因为它非常小，因此非常适合可穿戴应用。USB 电源组为微控制器和 led 提供电源。

TinyPico 使用其 WiFi 连接来查询服务器，该服务器从单独的传感器单元获得空气质量数据。项链以冷色调显示平静呼吸动画。然而，当空气质量恶化时，它会以更明确和充满活力的方式显示更温暖和更热的颜色。

这是一个巧妙的项目，展示了[极客 Faye]在电子和有品味的可穿戴制造方面的能力。构建既实用又舒适的项目并不总是容易的，但这个项目在这两方面都有效。GitHub repo 中包括项链的 3D 文件和微控制器固件代码，供那些热衷于深入了解细节的人使用。

这些年来，我们已经看到了一些很棒的项链，包括那些依靠一些[美丽的 PCB 艺术。](https://hackaday.com/2020/04/07/pcb-mill-turns-out-stylish-necklace/)休息后的视频。


 [https://www.youtube.com/embed/niAL5Nqm1jY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/niAL5Nqm1jY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

