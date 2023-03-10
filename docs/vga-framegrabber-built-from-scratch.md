# 从头开始构建的 VGA 帧抓取器

> 原文：<https://hackaday.com/2020/06/21/vga-framegrabber-built-from-scratch/>

现代计算机充满了各种各样的数字视频接口。DVI、HDMI、DisplayPort 都是这样的例子。在过去，VGA 主宰一切，将视频作为模拟信号发送到显示器。然而，将它转换回数字格式是可能的，[和【vihapuu】已经用他的 Grabor 项目做到了。](https://www.rpg.fi/desaster/blog/vga-framegrabbing-with-tvp7002.html)(下面还嵌入了演示视频。)

该项目依靠德州仪器 TVP7002 来完成将 VGA 转换为数字信号的艰巨工作。然后，该芯片的输出由 CPLD 拾取，并将结果数据写入 SRAM。借助微芯片 ENC28J60 以太网控制器，恩智浦微控制器负责从 SRAM 获取数据，并通过网络接口发送出去。

我们可以想象这种工具在通过网络使用复古机器时会很方便。我们以前也见过其他有趣的 VGA 黑客，比如这个基于 EEPROM 的信号发生器。休息后的视频。

 [https://www.youtube.com/embed/8bmWkqSN7pw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/8bmWkqSN7pw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

