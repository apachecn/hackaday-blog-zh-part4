# 使用 MQTT 和家庭助手的自动百叶窗

> 原文：<https://hackaday.com/2021/09/26/automated-window-blinds-using-mqtt-and-home-assistant/>

芬兰软件工程师[Toni]正在寻求使他 1991 年的房子现代化，他的最新项目是使用家庭助手自动控制百叶窗。除非你的百叶窗有内置电机，否则这种项目的大部分努力都集中在如何集成和连接电机上——正如[Toni]指出的，有大量不同的百叶窗，有各种各样的操作机制。但是一旦你解决了这个问题，就成功了一半。

这些特殊的百叶窗从完全打开到完全关闭只需要不到一圈的控制杆，而[Toni]选择了一个 270 度运动范围、20 千克*厘米扭矩的伺服电机来驱动它们。他很想把马达安装在窗户里面，但是就是装不进去。相反，每个伺服电机都安装在一个定制的 3D 打印盒中，该盒安装在操作杆正下方的窗框上。基于 ESP8266 的控制器盒安装在窗户上方，隐藏在窗帘后面，并操作所有三个伺服系统。

在软件方面，该项目是用 C++编写的，并使用 Ardiono IDE 上传。盲人使用 MQTT 与[Toni]的家庭助理网络通信。所有的软件都可以在[项目的 GitHub 库](https://github.com/kotope/blinds2mqtt)上获得，3D 打印的案例设计在[发布在 Thingiverse](https://www.thingiverse.com/thing:4946890) 上。即使你的百叶窗可能是完全不同的设计，我们认为[Toni]项目的许多部分仍然有用——如果你想做类似的事情，一定要看看这个项目。电动窗帘的概念已经存在一段时间了——我们在 2013 年和 2016 年分别报道了[的一个项目。如果你已经给你的百叶窗添加了自动化功能，请在评论区告诉我们效果如何。](https://hackaday.com/2013/04/18/hidden-servo-automates-slat-style-window-blinds/)

 [https://www.youtube.com/embed/B6eSw00hkLE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/B6eSw00hkLE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

