# 廉价派对灯获得 Arduino 升级

> 原文：<https://hackaday.com/2020/06/06/cheap-party-light-gets-arduino-upgrade/>

如果你有一个即将到来的派对，并且想要增加一点刺激，[你可能会对来自【Gav Lewis】](https://github.com/ferociousdiablo/arduflower)的这个最近的项目感兴趣。这款灯是基于市场上可以买到的派对灯，但是通过一些升级的组件，最终的产品比原来的更亮更有活力。

实际上，[Gav]已经改变了这种灯的几乎每个组件，除了外壳和前置镜头。原来的 5 毫米 LED 阵列被新的 8×8 WS2812B 面板取代，电子设备完全被 Arduino Nano 取代。他仍然使用 light 的原始电源，但由于它只能输出 4.2 伏左右的电压，他添加了一个升压转换器，为新硬件提供稳定的 5 伏电压。他还增加了一个 12 V 的冷却风扇，他说这基本上是无声的，因为它只有额定电压的一半。

[Gav]已经用 FastLED 开发了许多照明模式，它们很好地模拟了您可能从昂贵得多的激光扫描仪中看到的东西。在休息后的视频中，你可以看到多种颜色的光束如何同时射出外壳，在对面的墙上投射图案。他说，他想恢复设备的原始声音激活模式，但截至目前还没有得到代码排序。

该项目使用现成的 ws 2812 b led 8×8 矩阵，但如果您发现自己需要将单个 led 拼凑成自己的阵列，[我们最近报道了一个很好的技巧，可以使它变得更简单一些](https://hackaday.com/2020/05/08/these-led-shades-will-blind-you-with-science/)。

 [https://www.youtube.com/embed/sVy2k0N5fuQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/sVy2k0N5fuQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

