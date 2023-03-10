# 3D 打印机排放监测量化恶臭

> 原文：<https://hackaday.com/2019/09/03/3d-printer-emission-monitor-quantifies-the-stench/>

虽然我们还不知道在 3D 打印机周围闲逛的长期影响，但不需要深入研究就能发现它们的排放是不健康的。闻起来有毒的东西通常是有毒的。尽管如此，即使我们已经有了成百上千个小时的印刷时间，逗留在这里看着印刷品的出现也是一件非常有趣的事情。

我们大多数人都会同意 ABS 比 PLA 更臭，这可能是因为它在熔化时会释放甲醛。PLA 可以被视为危害稍小，因为它具有较低的熔点，并且在较高的温度下释放更多的挥发性有机化合物(VOCs)。虽然我们可能应该在印刷时总是打开一扇窗户，但人性是一种强大的力量。我们需要一些东西来拯救我们的固执，而[Gary Peng]有了答案:[一个智能 3D 打印机排放监测器](https://hackaday.io/project/167424-smart-3d-printer-emission-monitor)。

该监测器持续检查空气质量，并收集有关挥发性有机化合物排放的数据。当 VOCs 在打印过程中升高时，用户会收到视觉、听觉和电话通知。绿色表示你很好，黄色表示打开窗户，红色表示 GTFO。休息后有一个简短的演示，也显示了手机界面。

该监控器的核心是 CCS811 气体传感器，它向粒子光子提供 VOC 数据。[Gary]构建了一个简单的 Blynk 界面来处理警报和绘制历史 VOC 读数。他有可用的代码和 STLs，所以让这成为你最后一次在幸福的半无知中观看打印的东西。

担心空气质量？[这是一款独立的便携式显示器，旨在量化会议中令人窒息的气氛](https://hackaday.com/2018/05/29/monitoring-air-quality-one-sleepy-meeting-at-a-time/)。

 [https://www.youtube.com/embed/VX-_Cv9xZlY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/VX-_Cv9xZlY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

