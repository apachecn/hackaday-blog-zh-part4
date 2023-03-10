# 把书桌抽屉变成飞行轭

> 原文：<https://hackaday.com/2020/10/17/turning-a-desk-drawer-into-a-flight-yoke/>

[Christofer Hiitti]发现自己的电脑上有了最新的微软飞行模拟器，但他订购的操纵杆仍需几周才能上市。于是他抓起一个 Arduino、电位计和一个按钮[组装成了一个多么可笑的轭架](https://www.google.com/url?q=https%3A%2F%2Fwww.reddit.com%2Fr%2Fflightsim%2Fcomments%2Fij72d1%2Fwas_told_youd_appreciate_my_sweet_rig%2F&sa=D&sntz=1&usg=AFQjCNEYTz1wzuDTzZcRLBZJFfudcDwSVw)。

这个黑客的天才之处在于[克里斯托弗]利用他的书桌抽屉来控制音调的方式。塑料铰链的一端连接到抽屉内的电位计上，另一端贴在桌子顶部。第二个罐子贴在抽屉的前面，用于俯仰控制，第三个罐子是油门。它工作得非常好，如下面的演示视频所示。

抽屉机制的线性可能不是很好，但对于临时解决方案来说已经足够好了。他使用的 Arduino Leonardo 基于 ATmega32u4，它有一个内置的 USB，并且有像 ArduinoJoystickLibrary 这样的库，计算机界面非常简单。当[Christopher]真正的操纵杆最终到来时，他用玩笑轭组件制作了一个[按钮盒](https://github.com/christoferjh/HID_buttonbox)来扩充它。

毫无疑问，微软飞行模拟器 2020 将在未来几年产生许多伟大的控制器和驾驶舱。我们已经报道了一个[新的游戏手柄构建、](https://hackaday.com/2020/09/03/3d-printed-flight-controls-use-magnets-for-enhanced-flight-simulator-2020-experience/)和一个 [3D 打印框架，将 Xbox 控制器变成游戏手柄](https://hackaday.com/2020/09/25/xbox-controller-gets-snap-on-joystick-from-clever-3d-printed-design/)。

> 听说你会喜欢我可爱的装备！来自 [flightsim](https://www.reddit.com/r/flightsim/)