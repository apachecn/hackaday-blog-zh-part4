# 家酿光学传感器帮助您的柴油通过烟度测试

> 原文：<https://hackaday.com/2022/06/27/homebrew-optical-sensor-helps-your-diesel-pass-the-smoke-test/>

我们都听说过冒烟测试，我们知道这是电子设备性能的最低标准。如果通电后它没有着火，你就可以进行更多的功能测试了。但是烟尘测试对汽车来说意味着其他的东西，尤其是那些柴油驱动的汽车。通过柴油尾气测试可能会成为一件苦差事。

为了更容易地通过这些测试，[詹尼斯·阿尔尼斯]发明了这种柴油废气监控器，可以测量他的汽车排放的不透明度。该传感器本身非常简单，模仿商业废气分析仪所使用的:一个 LED 和一个光电二极管在一个特定长度的管的相对两端。通过管道的废气中的煤烟颗粒将以可预测的方式散射光，数字计算出通过等级是大于 53%的透射率。

传感器主体由黄铜管件拼凑而成，两端都用环氧树脂粘合了玻璃窗。废气通过连接到软管和取样管的三通接头进入，并通过另一个三通接头排出。传感器的一个窗口有一个廉价的电池供电的手电筒作为光源，另一端有一个德州仪器 OPT101 光电二极管传感器。该传感器连接到 Arduino 的一个模拟输入端，Arduino 还运行一个 128×64 像素的 LCD 显示器——受空气质量计的启发——以图形和百分比的形式显示当前的烟雾状况。下面的视频显示了工作中的传感器。

虽然煤烟堆积和水蒸气冷凝存在一些问题，但使用传感器[Janis]发现，一点点预热驱动就足以消除他的座驾冒烟的倾向，使他通过检查。

 [https://www.youtube.com/embed/q2FEBz9Ials?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/q2FEBz9Ials?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

