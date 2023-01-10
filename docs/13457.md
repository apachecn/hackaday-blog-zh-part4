# 用 Python 和乐高搭建反作用轮

> 原文：<https://hackaday.com/2022/04/27/building-reaction-wheels-with-python-and-lego/>

反作用轮是很有用的东西，通常被卫星用来在太空中保持正确的方向。转动反作用轮会在航天器中产生一个大小相等方向相反的扭矩，使其能够准确地指向和旋转。同样的技术也适用于地球，并且[砖块实验频道]决定用乐高建造一个来控制倒立摆。

最初的设计是在倒立摆上使用一个小乐高轮，只能在与垂直方向成 4 度角的范围内可靠地工作。将车轮升级到更大、更重的车轮使车轮能够在 28 度的范围内工作。

MPU9250 惯性测量单元被用于控制反作用轮，安装在摆锤的底座上，并由 Raspberry Pi 读取。Pi 获取加速度计和陀螺仪的读数，然后用 PID 控制器控制摆上的电机，使倒立摆保持直立。

该视频详细介绍了如何让钟摆平稳运行。从控制系数的变化到测量电机的反电动势，[砖块实验频道]展示了使钟摆对外界扰动具有鲁棒性所需的一切。

正如我们一次又一次看到的，倒立摆是学习控制理论的好方法。

 [https://www.youtube.com/embed/WObG2LoSEwQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/WObG2LoSEwQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

