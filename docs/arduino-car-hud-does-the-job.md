# Arduino Car HUD 可以完成这项工作

> 原文：<https://hackaday.com/2020/06/03/arduino-car-hud-does-the-job/>

如今，许多汽车都配备了基本的平视显示器(HUD)。通常，这些显示速度，虽然有些也扔在一个转速表或导航图形。当然，如果你的车没有这些库存，你也可以选择改装自己的车。

[PowerBroker2]以一种有点迂回的方式开发了这个 HUD，但它仍然是有效的。ELM327 蓝牙 OBD-II 阅读器连接到汽车上，收集速度和转速数据。该数据被传递给 ESP-32 和 Teensy 3.5。通过阅读代码，似乎 Teensy 负责将来自 CAN 总线的数据记录在 SD 卡上，并运行一个小型有机发光二极管显示器。然后 ESP32 负责运行实际形成 HUD 的 LED 显示器。然后，它与 3D 打印的外壳、一些有机玻璃和反射挡风玻璃膜相结合，以完成这一效果。

这个版本可能包含了比完成工作严格需要的更多的硬件，但它确实完成了工作。我们见过的其他建筑使用 LED 灯带作为一种快速、整洁的方式来完成工作。休息后的视频。

 [https://www.youtube.com/embed/JxBvukUipc4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/JxBvukUipc4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

