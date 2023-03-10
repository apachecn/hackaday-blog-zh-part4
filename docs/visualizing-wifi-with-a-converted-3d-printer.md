# 使用转换后的 3D 打印机可视化 WiFi

> 原文：<https://hackaday.com/2021/11/22/visualizing-wifi-with-a-converted-3d-printer/>

我们都知道我们生活在电磁辐射的汪洋大海中，从调幅无线电广播到宇宙射线，无所不包。有些是有用的，有些是讨厌的，但所有的都是看不见的。我们知道它在那里，但我们不知道田野是什么样子。当然，除非你把类似于[这个 3D WiFi 场强可视化器](https://github.com/Neumi/3D_wifi_scanner)的东西投入使用。

诚然，【Neumi】的 WiFi 扫描仪是基于一台老式 3D 打印机的机架，工作范围有些有限。NodeMCU ESP32 模块位于打印机挤出机通常所在的位置，并扫描一系列相距一厘米的点。在每个点从 NodeMCU 的 WiFi 获取接收信号强度指示器(RSSI)读数，并将每个点的位置和 RSSI 数据保存到 CSV 文件中。然后，几个 Python 程序对原始数据进行消化，产生 2D 和 3D 扫描。3D 扫描是最具启发性的——你实际上可以看到 12.5 厘米的信号强度间隔，这对应于 2.4 GHz WiFi 的波长。下面的视频展示了数据采集过程和一些可视化效果。

虽然在这个规模下仍然很酷，但我们希望看到这个规模扩大。[Neumi]已经做了一个大规模的 3D 可视化项目，[使用超声波而不是无线电波](https://hackaday.com/2021/09/06/homebrew-sounder-maps-the-depths-in-depth/)，所以他在这方面有一些经验。但是也许[一个电缆机器人](https://hackaday.com/2015/09/21/3d-cable-robot-uses-the-building-as-its-exoskeleton/)或者类似的东西可以用于一个房间大小的实验。一个不错的办法是使用 SDR 加密狗来收集信号强度数据，这将允许您查看频谱的不同部分。

 [https://www.youtube.com/embed/COI6knr9qPM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/COI6knr9qPM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

