# 黑进梅卡蒙机器人来增加新的能力

> 原文：<https://hackaday.com/2021/11/03/hacking-the-mekamon-robot-to-add-new-capabilities/>

来自 Reach Robotics 的 Mekamon 是一个整洁的东西，一个由手机应用程序控制的机器人，用四条腿走路。[韦斯·弗里曼]决定黑掉这个平台，给它一个传感器包，并在这个过程中实现一些基本的自主行为。

[Wes]开始使用数据包嗅探器找出通过蓝牙控制 Mekamon 机器人的命令系统。然后，他开始在机器人上安装树莓 Pi 3，并在装有万向摄像头的摄像头上安装 Pi 相机。

在 Raspberry Pi 上运行 OpenCV 使 Mekamon 机器人能够跟随放置在其视野中的彩球。后来的工作包括将硬件升级到 Pi 计算模块 3，其双摄像头输入允许使用立体成像设置。

所有部件都简单地安装在原始机器人的顶部，不需要永久性的改变。这是一种巧妙的黑客攻击方式，通过扩展原有的功能，而实际上不必在内部进行改动。

这些年来，我们已经看到了大量的自主建造，从农业机器人到旨在探索城市环境的机器人。休息后的视频。

 [https://www.youtube.com/embed/FjHKsbVByhM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/FjHKsbVByhM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

