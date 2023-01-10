# 3D 打印机自制探头:3 美元

> 原文：<https://hackaday.com/2022/02/11/homemade-probe-for-3d-printer-3/>

如果您想使用探针来调平 3D 打印机底座，您有几个选择。很少会看到光学或电容探头。不过，更常见的情况是，您的探针会感应到金属印迹，或者使用物理探针接触印刷层。【设计原型测试】早就用了一个 BLTouch，它使用的是后一种方法。然而，将它放在加热的建造室中会妨碍它的工作，所以他开始用内六角扳手制作自己的简单设计。

我们以前见过内六角传感器，但通常情况下，它们使用微动开关。我们也看到了用来直接探测床的微型开关。但是，在这种情况下，3D 打印的风扇罩使用光学传感器来记录艾伦内六角扳手何时碰到床。

我们真正喜欢的是半手动的收回装置。在正常操作过程中，磁铁会将扳手托起。在你回家或探测床之前，你从磁铁上松开扳手。当你完成的时候，你能再次停放它。不需要伺服电机或任何其他电气设备。

它看起来非常合理，10 次测量的范围小于 0.05 毫米。不太好，但 3 美元也不错。我们正在等待即将到来的 STLs。但是，您可以很容易地将这种想法应用到您的特定打印机设置中。此外，还计划通过一个小的重新设计来提高精确度。

我们最近讨论了 Marlin 如何实现[统一基床调平](https://hackaday.com/2022/01/05/3d-printering-one-bed-level-to-rule-them-all/)，这个探测器将为此工作。还有一种趋势是把[传感器放在喷嘴](https://hackaday.com/2021/08/30/3d-printering-is-hassle-free-bed-leveling-finally-here/)里，这有它的利弊。

 [https://www.youtube.com/embed/xqttz2IZ6ko?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/xqttz2IZ6ko?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

