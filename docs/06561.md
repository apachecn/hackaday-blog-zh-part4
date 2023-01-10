# 软驱键盘是低效的乐趣

> 原文：<https://hackaday.com/2020/05/13/floppy-drive-keyboard-is-inefficient-fun/>

我们大多数人都习惯于在机器上使用典型的 101 键打字设置。多年来，移动和触摸屏设备已经提供了替代界面，但通常仍坚持 QWERTY 或其他类似的布局。[foone]不在乎传统，然而，[基于标志性的软盘构建一个文本输入设备。](https://twitter.com/Foone/status/1259644761209634818)

构建从一个标准的 PC 软驱开始，连接到一个接口板，允许它通过 USB 工作。它连接到一个 Raspberry Pi，运行一个 Python 程序监听媒体插入事件。当检测到新磁盘时，它会读取卷标，并将其发送到一个 Teensy LC，该 LC 模拟连接到主机的 USB 键盘。该设置使用 29 个磁盘，从 A 到 Z，！、移位和空格。所有这些都装在 SCSI 磁盘盒中，该磁盘盒有助于提供电源以及经典的米色 90 年代美感。

虽然你可能不会就此事打出你的论文，但这是一个很好的话题。[我们之前也介绍过一些[foone]的折衷作品](https://hackaday.com/2019/02/21/death-generator-makes-game-over-more-personal/)。休息后的视频。

 [https://www.youtube.com/embed/Rb42ud2SY00?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Rb42ud2SY00?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

