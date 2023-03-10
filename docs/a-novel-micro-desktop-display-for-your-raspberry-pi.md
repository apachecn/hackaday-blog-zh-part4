# 一个新颖的微型桌面显示器为您的树莓皮

> 原文：<https://hackaday.com/2020/12/31/a-novel-micro-desktop-display-for-your-raspberry-pi/>

自 2012 年首次亮相以来，已经有多种创造性的展示与树莓派一起使用。也许你还记得重新设计的摩托罗拉电话坞站，或者你有一个插入扩展端口的小显示器。不可避免地，较小的选项作为桌面显示器变得令人失望，因为虽然广告胜利地展示了他们炫耀一个树莓 Pi OS 桌面，但现实几乎是不可用的。直到现在。

随之而来的是[igbit]的解决方案[，它是一个小型 SPI 显示器，以不同的方式显示桌面](https://github.com/igbit/micro-displays)。它不是在整个屏幕上显示一个火柴盒大小的桌面，而是分成两半。顶部是桌面的表示，而下面是鼠标指针周围区域的特写。

出乎意料的是，它的操作模式对于非 Linux 专家来说非常容易理解，因为它通过一个 Python 脚本来工作，该脚本可以截取两个区域的屏幕截图，并将它们作为一个组合传递给显示器。在鼠标指针周围绘制了一个放大窗口大小的区域，使鼠标指针可以很容易地定位在微小的桌面上。它依赖于主显示器被推送到 HDMI 输出，因此，如果 Pi 是无头的，那么它的配置必须强制使用 HDMI。结果并不能帮助您完成要求更高的桌面任务，但是它提供了一个简洁的解决方案，能够在一个小屏幕上使用 Pi 桌面。

当然，在紧要关头你可以随时使用你的手机。