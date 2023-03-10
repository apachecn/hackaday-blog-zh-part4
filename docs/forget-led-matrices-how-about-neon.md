# 别管 LED 矩阵了，霓虹灯怎么样！

> 原文：<https://hackaday.com/2020/07/18/forget-led-matrices-how-about-neon/>

低成本 LED 已经改变了我们所有形式的照明方式，允许复杂的可寻址显示器和各种照明。但是在我们有廉价的 LED 阵列之前，我们做了什么呢？或许，用霓虹灯？这正是[Manawyrm]在他的[可链接的 8×8 霓虹灯矩阵板](https://github.com/Manawyrm/NeonMatrix)上所做的，它采用 64 个霓虹灯灯泡，并用单独的三端双向可控硅开关从电源电位驱动每个灯泡。一系列 74HC595s 处理数据传输，在电源电压下浮动，而其 ESP32 驱动器通过一组隔离器保持安全。

一篇 Twitter 帖子[展示了它的实际运行](https://twitter.com/Manawyrm/status/1280229457828200449)，但也许最值得称赞的应该是他的测试设备。由于无法获得测试阵列的可变 230V 主电源，他将 50 Hz 正弦波应用于音频功率放大器，[用主变压器的低压侧代替了扬声器](https://twitter.com/Manawyrm/status/1280235348946280449)。这是我们忍不住喜欢的那种恶作剧。

在这里，近地天体通常被描述为新奇的事物，而不是它们自身的重要展示。它们是有趣的组件，每个人都应该玩一玩，尤其是因为它们具有负电阻，并且[可以振荡。](https://en.wikipedia.org/wiki/Pearson%E2%80%93Anson_effect)