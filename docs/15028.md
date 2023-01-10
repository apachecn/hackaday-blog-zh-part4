# 蓝牙接口为 Commodore 64 游戏增加了隆隆声反馈

> 原文：<https://hackaday.com/2022/10/08/bluetooth-interface-adds-rumble-feedback-to-commodore-64-games/>

没有什么比带有一个红色开火按钮的黑色操纵杆更能代表“20 世纪 80 年代的游戏”了。但是如果你喜欢更好的人体工程学，你可以通过各种现代到经典的接口适配器将现代游戏手柄连接到你的复古电脑上。这些设备通常只支持方向板和一两个动作按钮，而忽略了运动控制和触觉反馈等现代功能。

这有点遗憾，因为我们认为每当陷阱哈利在流沙中溺水或青蛙被交通事故击中时，在我们手中感受到电击会很酷。因此，我们很高兴地宣布，[Ricardo Quesada]已经决定[为他一直在开发的蓝牙到操纵杆端口接口](https://retro.moe/2022/10/02/gamepad-rumble-support-for-the-commodore-64/)添加隆隆声功能。他在休息后嵌入的视频中演示了他的 Commodore 64 上的功能。

自然，任何软件都需要适应支持触觉反馈，但一个更棘手的问题是硬件:操纵杆端口是只输入设备，因此不能向任何连接的游戏手柄发送“启用隆隆声”信号。[Ricardo]找到了一个巧妙的方法，使用操纵杆端口上的模拟输入，这些输入通常用于桨式控制器。

计算机内部的模数转换器通过向模拟端口施加脉冲信号并测量电容器放电所需的时间来工作。现代游戏手柄界面只是检测这些脉冲是否存在；它们可以通过软件切换操纵杆端口上的模拟读数来启用或禁用。这样，操纵杆端口就可以用来向任何与之相连的设备发送一位信息。

[李嘉图]为*兰博:第一滴血第二部*和*莱曼*开发了补丁来启用隆隆功能。他在博客中详细描述了这一过程，这将使任何了解 6502 机器代码的人能够为他们喜爱的游戏添加隆隆声支持。

该适配器适用于各种使用 Atari 风格操纵杆接口的复古系统，但如果你是 Apple II 用户，你可能想看看[这个基于 Raspberry Pi 的项目](https://hackaday.com/2016/08/03/an-apple-ii-joystick-fix-for-enjoyable-gameplay/)，它与其非标准操纵杆接口相接口。如果你喜欢无线游戏，一定要看看我们的[无线游戏控制器的历史](https://hackaday.com/2018/12/10/the-evolution-of-wireless-game-controllers/)。

 [https://www.youtube.com/embed/vCj45OX43JE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/vCj45OX43JE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

