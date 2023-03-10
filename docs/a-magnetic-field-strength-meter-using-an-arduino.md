# 使用 Arduino 的磁场强度计

> 原文：<https://hackaday.com/2021/04/04/a-magnetic-field-strength-meter-using-an-arduino/>

我们习惯将霍尔效应器件作为机械系统中的近程传感器，用于检测附着有磁铁的物体。然而，人们很容易忘记，提供磁性或非磁性数字输出的设备只是故事的一部分，线性霍尔效应设备提供了一种测量静态磁场的简便方法。这是[mircemk]展示的东西，用的是一个 Arduino 供电的磁场强度计，它使用了一个 UGN 3503U 霍尔效应设备。

电路非常简单，包括传感器、Arduino Nano 和有机发光二极管显示器。该器件非常方便，因为它的电压输出与传感器的高斯电平有已知的关系，因此虽然其校准的准确性未经验证，但它至少可以从 Arduino 的 ADC 中获得可信的读数。

整个包裹在一个吸引人的外壳中，看起来好像是由 PCB 材料制成的，传感器突出在似乎是塑料圆珠笔的外壳上。它是一个方便的工具，用不了多少钱就能提供有用的功能，有什么不喜欢的呢！完整的故事请看下面的视频。

令人惊讶的是，这样的项目在 Hackaday 很少，然而[这不是我们第一次看到磁场测量](https://hackaday.com/2016/07/16/hackaday-prize-entry-measuring-3d-magnetic-fields-needs-prize-footer/)。

 [https://www.youtube.com/embed/zoQZeYq9ybI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/zoQZeYq9ybI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

