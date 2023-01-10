# 树莓 Pi 绘制世界范围的地震

> 原文：<https://hackaday.com/2021/10/05/raspberry-pi-plots-world-wide-earthquakes/>

当你偶然发现一个发布实时地震数据的网站时，你会怎么做？好吧，如果你是[克雷格·林德利] [你写一些代码把它很好地格式化到显示器上](http://craigandheather.net/celeearthquakemap.html)，把它放在一个盒子里，边做晚餐边看。

[Craig]开始在 ESP32 上用 Forth 编码，使用的是 [ESP32Forth](https://esp32forth.appspot.com/ESP32forth.html) ，但他承认进展不太顺利，放弃了 ESP32，用他手头的一个 Raspberry Pi 3，经过 C++的短暂迂回后，他决定用 Pygame 实现 Python。

一个盒子是 3D 打印的，他说效果不错，但需要一点调整才能完美。官方 7 英寸显示屏的 Pi 并不缺少外壳选项，[Craig]认为 3D 打印外壳可能不值得，如果他再次建造它，可能会使用更适合的商用选项。

当开发代码并观察它的工作时，他注意到夏威夷周围的地震群，然后他发现基拉韦厄火山刚刚上升。哇哦。

对于类似的拍摄，请查看使用 ESP32 和相同数据源的另一个最近的构建。