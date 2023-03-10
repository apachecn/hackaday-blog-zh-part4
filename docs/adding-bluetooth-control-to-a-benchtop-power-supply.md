# 将蓝牙控制添加到台式电源

> 原文：<https://hackaday.com/2019/06/10/adding-bluetooth-control-to-a-benchtop-power-supply/>

2019 年，有可能以比以往任何时候都更便宜的价格为实验室配备所有必需品。DPS3005 就是这种低成本设备的一个例子，它是一种可变电源，价格不到 50 美元，功能齐全。然而，[Markel Robregado]想要更多的功能，于是开始着手工作。

[Markel]项目的关键是改善连通性。德州仪器公司的 CC2640R2F 发射台被用来运行该节目，其蓝牙低能耗功能将派上用场。一个定制的智能手机应用程序与 Launchpad 通信，然后 launch pad 通过其串行 Modbus 接口与电源通信。通过该应用程序，[Markel]可以设置电源的电压和电流限制，以及开关电源。这可能证明是有用的，特别是在处理危险项目的情况下用于远程触发。毕竟，有时候躲起来是值得的。

我们以前见过电源被修改过；这种高精度的锅模是一种特殊的享受。如果您为了获得更好的性能而入侵了您的硬件平台，请告诉我们。休息后的视频。

 [https://www.youtube.com/embed/Kn_xyTP1LDk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Kn_xyTP1LDk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

