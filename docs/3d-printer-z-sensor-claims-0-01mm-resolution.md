# 3D 打印机 Z 传感器声称分辨率为 0.01 毫米

> 原文：<https://hackaday.com/2022/11/14/3d-printer-z-sensor-claims-0-01mm-resolution/>

早期的 3D 打印机通常有一个微型开关，让你知道 Z 轴何时位于零点。通常有一个调节螺丝，所以你可以调整到正确的层高度。但是现在，你最常看到的是某种传感器。也有感应传感器，可以与金属床和一些其他类型的床一起工作。然而，最常见的是“BL touch”型传感器，它将探头放在喷嘴下方，进行测量，然后收回探头。然而，几乎所有这些传感器都是通过检测床的特定高度来工作的，仅此而已。

一个名为 BDsensor 的新探针是感应式的，但可以实时读取床的高度。根据开发商提供的信息，它实现了 0.01 毫米的分辨率和+/-0.005 毫米的可重复性。我们不知道这是真是假，但能够实时探测喷嘴高度会带来一些有趣的可能性，如实时调整 Z 高度，如下面的视频所示。

该设备确实需要校准。实际上，您将喷嘴向下接触到床，机器的尺寸为 7 毫米，并在此过程中建立校准曲线。Marlin 的最新版本支持探头，并在 LCD 上实时显示测得的高度。您确实需要两个空闲的 I/O 引脚，但由于 BL Touch 也需要，您可能有一个可以使用的端口。

在使用中，你可以观看实时显示来帮助你手动调平，或者使用该装置作为传统的探针来自动调平。您还可以设置动态调平，如视频所示。床传感器[不一定很贵](https://hackaday.com/2022/02/11/homemade-probe-for-3d-printer-3/)，但不断测量床的高度似乎是这种探头最独特的地方。

对于一个相当便宜的设备来说，这些都是相当大的要求。你用过吗？如果是这样，请在评论中告诉我们它对你有什么帮助。

 [https://www.youtube.com/embed/yx8pluEu0sg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/yx8pluEu0sg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

