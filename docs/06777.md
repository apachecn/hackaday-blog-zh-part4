# 使用此扬声器模块将 MicroKORG 变成 MicroKORG S

> 原文：<https://hackaday.com/2020/06/05/turning-a-microkorg-into-a-microkorg-s-with-this-speaker-mod/>

当[Michael Wessel]购买他的 MicroKORG 合成器/声码器时，两年后 MicroKORG S 发布时，他并不觉得有趣，因为“S”代表“声音”，显然是添加了 2+1 扬声器系统。不为所动，[Michael]发现这两个合成器非常相似，可以在原来的 MicroKORG 上添加一个相似的扬声器系统[。](https://hackaday.io/project/172154-loudspeaker-your-microkorg)

当人们比较[的原版](https://www.korg.com/us/products/synthesizers/microkorg/)和它的[继任者](https://www.korg.com/us/products/synthesizers/microkorg_s/index.php)时，这两款产品之间的相似之处变得显而易见，后者似乎主要增加了所述扬声器和更多预设，以及时髦的新外观。(虽然原版的 70 年代造型可能粉丝更多。)正如嵌入的视频所示，这个 mod 相当干净。

这个模块的核心是一个基于 [PAM8403](https://www.diodes.com/assets/Datasheets/PAM8403.pdf) 的 D 类放大器板。PAM8403 是一款 3 W 音频放大器，最初由 Power Analog Microelectronics(现为 Diodes)生产。虽然不是一款出色的放大器，但它非常适合 MicroKORG 等电池供电应用。完成构建的是一个 7805 线性调节器，用于为 PAM8403 提供 5 V 电压，几个滤波电容，一个开关，用于打开/关闭扬声器，当然还有扬声器。

虽然外壳中有相当大的空间，但大多数扬声器都足够大，可能会有点挤。[Michael]找到了一些低调的 20 W 全频扬声器，它们似乎很适合这个目的。要完成布线，只需要一个孔锯和一种从 MicroKORG 获得音频输出的方法。

在这种模式下，[迈克尔]选择从后面的输出插孔获得音频，但为了更清晰的结果，它可能会直接连接到板上的标题。

 [https://www.youtube.com/embed/C0g_5m_lPxk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/C0g_5m_lPxk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

