# 夏克电台短波数字化

> 原文：<https://hackaday.com/2020/05/20/radio-shack-shortwave-goes-digital/>

如果你在 20 世纪 70 年代沉迷于浏览 Radio Shack 目录，你可能还记得 DX-160 短波接收机。你可能已经有一个了。这款收音机看起来可疑地像同一时代价格较低的 Eico，但它有着令人惊叹的宽带拨号，而不是 Eico 未校准的 1 到 10 号旋钮。找到一个精确的频率是一个使用两个旋钮的巧妙过程，但是[弗兰克]决定用一个数字频率显示器改装他的。

即使你没有 DX-160，弗兰克使用的技术也非常适用于像这样的旧接收机。在这种情况下，收音机是一个带有可变频率振荡器(VFO)的单变频超外差，因此您只需读取该频率，然后在显示前加上或减去 IF。如果你能找到一个不干扰 VFO 的地方，你应该能做同样的特技。

在这个接收器的全盛时期，这将是一个令人生畏的项目。今天，一个便宜的数字显示器就可以了。事实证明，这台收音机有一些波段调到 VFO 频率负 455 千赫，还有一些波段调到 VFO 频率正 455 千赫。有了微控制器，你可以很容易地处理这个问题，但[弗兰克]的解决方案是简单地使用两个显示器。他们很便宜，为什么不呢？显示器是可配置的，所以即使你不得不手动打开开关，你也能找到使用它的方法。

显示器从收音机的灯座获取电能。该项目的真正诀窍是找到一个地方来挖掘 VFO 频率，然后以一种不会杀死振荡器或引入不稳定性的方式这样做。[Frank 的]设计使用一个电容器将振荡器的能量耦合到计数器中。

如果你不想使用现成的显示器，用大多数微控制器计算频率是很容易的。一些公司为此配备了专用硬件。一个常用的技巧是计算一段时间内过零点的次数，并换算成一秒钟内过零点的次数。然而，有各种各样的方法。

我们不得不承认，在享受老式收音机的同时，我们也享受着数字显示器。当然，另一个答案是[完全取代 VFO](https://hackaday.com/2016/03/05/teensy-3-1-controlled-vfo/)，但这将否定酷旧的表盘。