# 黑客入侵 IPod Nano 显示器:漂亮！

> 原文：<https://hackaday.com/2019/03/06/hacking-the-ipod-nano-display-beautiful/>

第六代 iPod Nano 在发布时是一个新发现。将彩色屏幕、音频硬件和可充电电池装入一个不比大邮票大的包装中，至今仍令人印象深刻。它们现在被用于各种 maker 项目的显示器，但如果你这样做，你可能会想如何建立一个图形界面。不要担心—[只要拿一个 ESP32 和合适的 GUI 库，就可以上路了。](https://blog.littlevgl.com/2019-02-02/use-ipod-nano6-lcd-for-littlevgl)

纳米屏幕使用 MIPI DSI 接口，这不是直接与 ESP32 一起使用的最简单的事情。相反，SSD2805 接口芯片将并行输入数据转换为 MIPI DSI 信号来驱动显示器。然而，驱动显示器只是游戏的一部分——你需要一些东西在上面显示。将 LittlevGL GUI 库与屏幕的触摸板相结合，可以轻松创建完整的图形界面。

随着直接针对制造商市场的显示产品的激增，黑客屏幕现在已经不常见了。然而，看到一个成功的黑客做得很好总是很棒的。我们也看到了显示器的逆向工程——[,这当然不容易。](https://hackaday.com/2013/12/14/reverse-engineering-an-lcd-display/)