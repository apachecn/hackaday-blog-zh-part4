# 快速原型法测量急流中的浊度

> 原文：<https://hackaday.com/2022/11/15/rapid-prototyping-to-measure-turbidity-in-rapids/>

[RiverTechJess]正在攻读环境工程博士学位，他专门用了一章的篇幅来开发用于河网监测的浊度传感器。环境感测受益于能够准确和频繁地测量，因此提供低成本设备有助于获得更多数据，并避免在野外部署电子设备时必然会发生的偶尔设备丢失。为此，[RiverTechJess]开发了一种[低成本浊度传感器](https://github.com/rivertechlabs/turbiditysensor),在成本和精度上可与更昂贵的替代产品相媲美。

浊度传感器被设计成至少部分浸没，以允许 LED 和光传感器能够进行测量。[RiverTechJess]已经制作了一个 3D 打印原型来测试设计，允许快速实验和部署传感器来解决问题。3D 打印的外壳原型使用橡胶 o 形圈和“真空油脂”来提供防水密封。ESP32 微控制器用于将记录的数据存储在 SD 卡上，并驱动 TSHG6200 850nm 纳米红外 LED 和两个 TSL237S-LF 传感器。

除了关于过程的[博客之外，关于浊度传感器的](https://rivertechlabs.org/blog/)[论文](https://www.nature.com/articles/s41598-022-14228-4)提供了大量数据，显示了开发和校准用于环境监测的设备的过程。所有的源代码都可以在 [GitHub](https://github.com/rivertechlabs/turbiditysensor) 上获得，开发工作将继续进行，开发浊度传感器的[新版本](https://github.com/rivertechlabs/suspendedsedimentsensor)，配备最新的电子设备和硬件。

我们对水传感器并不陌生，我们见过从[联网水污染监测器](https://hackaday.com/2022/04/02/monitoring-water-quality-using-lots-of-sensors-and-machine-learning/)到小型[手持饮用水探测器](https://hackaday.com/2020/08/29/unifiedwater-finds-potable-water-and-stops-polluters/)的设备。

休息后的视频！

 [https://www.youtube.com/embed/s__AqbmApyk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/s__AqbmApyk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

