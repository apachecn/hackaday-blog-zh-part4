# 产量翻了四倍的 3D 打印机

> 原文：<https://hackaday.com/2022/10/19/a-3d-printer-with-quadruple-the-output/>

虽然测谎仪在口语中与伪科学测谎仪测试联系在一起，但第一台测谎仪的实际发明是为了机械复制某人书写的笔画。众所周知，美国前总统托马斯·杰斐逊在他的“现代办公室”中使用了测谎仪，其复制品仍保存在史密森尼博物馆。我们中很少有人再需要笔式测谎仪了，但是仍然可以从这种机器中收集到这个百年发明的灵感，[就像这台 3D 打印机，它可以一次输出四张相同的照片](https://www.youtube.com/watch?v=DpHZpsEhN6A)。

打印机是一个核心 XY 设计，有四个独立的打印头，它们都锁定在一起。打印机的表现就像只有一个打印头，这使它比其他情况下更简单。需要额外考虑印刷床，以确保其水平和平坦，它还包括一个独特的 Z 轴，旨在防止低质量丝杠的 Z 带。它有一个相当宽的打印区域，但一个明显的限制是，它基本上是四分之一，所以虽然它可以一次生产许多零件，但它不能生产一个使用整个打印床区域的零件。

用于制造这台打印机的每一个打印部件都是由[Rick]在 OpenSCAD 中设计的。他还用打印机驱动程序和 KiCad 中的所有其他相关电路构建了一个定制的电子板。对于任何打印大量零件的人来说，这可能只是增加产量而不必管理更多打印机的诀窍。如果你已经有了更多的打印机，并且需要一种更简单的方式来管理它们，看看这个专用的 Raspberry Pi 就可以了。

 [https://www.youtube.com/embed/DpHZpsEhN6A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/DpHZpsEhN6A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

