# ESP32 串行接口使旧设备现代化

> 原文：<https://hackaday.com/2020/01/27/esp32-serial-interface-modernizes-old-equipment/>

仍然有很多有用的硬件使用 RS-232 接口，比如[Lasse Lukkari]不时使用的百灵达 Ultradrive 扬声器系统。他没有因为现代电脑(更不用说手机或平板电脑)没有物理串口而放弃完美的设备，而是决定为这些旧设备开发一个 WiFi 适配器，他称之为 SerialChiller。

SerialChiller 内部有一个 ESP32、一个 MAX3232 线路驱动器、一个 LM1117 线性调节器和几个无源器件。专业制造的 PCB 封装在一个外壳内，[Lasse]从一个便宜的 DB15 分支适配器改造而来。USB 电缆用于为电路板供电和编程，但也可用于将串行冷却器转换为 USB 转串行电缆。

这个项目的硬件非常简单，但我们真正喜欢的是他在软件方面的方向。[Lasse]实际上是直接在微控制器上实现一个完整的基于网络的界面，而不是将 SerialChiller 用作一个简单的串行到 WiFi 的网桥。在休息后的视频中，他展示了控制上述百灵达 Ultradrive 的固件，但这只是该项目的一个可能的应用。固件可以为各种经典设备升级，为硬件注入新的生命，否则这些硬件可能会面临被扔进垃圾填埋场的危险。

当然，[使用 ESP 系列芯片作为串行适配器并不是什么新鲜事](https://hackaday.com/2015/10/23/use-the-esp-as-a-serial-adapter/)。事实上，这就是它们的设计目的。但是，由于 ESP32 的强大功能，为旧硬件开发现代用户界面具有一些迷人的潜力。

 [https://www.youtube.com/embed/Z5CDjev1ydA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Z5CDjev1ydA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

