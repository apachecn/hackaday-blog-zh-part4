# 使用轻触开关和硬币电池的 3D 打印机底座探测

> 原文：<https://hackaday.com/2021/10/26/3d-printer-bed-probing-using-a-tact-switch-and-coin-cell/>

受 CNC 调平系统的启发，[Chuck]制作了一个小 PCB 来[帮助调平他的 3D 打印机](https://www.youtube.com/watch?v=715Xop79Sus)，他在下面的视频中分享了细节。这个想法很简单，喷嘴向下压在 PCB 上，PCB 下面有一个轻触开关。当开关闭合时，LED 灯亮。

在实践中，您测量电路板的高度，并将其用作 Z 偏移，这样就完成了。我们唯一关心的是开关的可重复性。诚然，大多数人使用一张纸，这可能是不完全可重复或准确的。合适的测隙规是“正确的”方法，但我们知道只有少数人这样做。

如果您曾经研究过各种 Z 探针的可重复性，如接近传感器或从 3D 触摸探针中脱落的小针，它们是不可重复的。有些人也使用[微型开关](https://reprap.org/wiki/Z_probe)，这与这种方法非常相似，显然已经足够好了。

该板是可用的，但它足够简单，您可以用几乎任何用于 PCB 的方法来创建它或等效物。[Chuck 的]原型板被铣削。我们总是很惊讶更多的人不使用喷嘴本身来感知床。有些人甚至为了 CNC 去了比电接触更多的[麻烦。](https://hackaday.com/2011/06/09/diy-cnc-touch-probe/)

 [https://www.youtube.com/embed/715Xop79Sus?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/715Xop79Sus?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

