# 自动计时，让教学变得轻松

> 原文：<https://hackaday.com/2020/04/16/automatic-timelapses-made-educational-and-easy/>

[![](img/4ff0b6097d2eaf868cfc559b47355d26.png)](https://hackaday.com/wp-content/uploads/2020/04/easy-timelapses-animation.gif)

Timelapse fragment from an infrared sky camera watching cloud patterns.

有很多方法可以创建延时视频，但[Andy]有一种有效的方法来确保他的红外天空相机有最新的视频，他让它运行是因为在一个备用的 Raspberry Pi 上有一些记录良好的 shell 脚本。由此产生的延时视频总是可以从网上获得，并且总是当天最新的。

这个想法是从一个远程来源(在他的例子中，是一个红外天空摄像机)自动获取图像，并将它们转换成一个累积的视频，该视频在当天定期更新。生成的视频文件要么从同一台机器上提供，要么发送到其他地方。除了剧照的来源之外，所需要的只是两个 shell 脚本和一些常见的 Linux 实用程序。

由于[安迪]主要对追踪云感兴趣，他的系统只在白天运行，但它可以很容易地改变。事实上，[Andy]的两个 shell 脚本是很好的项目资源，不仅因为它们易于修改并且有很好的文档记录，还因为他没有假设一个人对命令行的了解程度。他还提供了来自经验的提示；例如，他发现 120 秒的间隔是最好的计时间隔。

[Andy]在 Raspberry Pi 4 上运行他的脚本，但是任何 Linux 系统都可以。对于那些可能更喜欢嵌入式方法的人来说，[ESP32-CAM 可以不费吹灰之力就制作出一台出色的延时相机](https://hackaday.com/2020/01/28/esp32-cam-does-time-lapse/)。