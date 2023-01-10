# 电动窗机构变成电动纱门

> 原文：<https://hackaday.com/2020/09/29/electric-window-mechanism-into-a-electric-screen-door/>

在世界上的许多地方，让门或窗开着是让房子充满虫子的好方法。对于人类成员来说，记住随手关门可能出奇地困难，所以[管道技工]使用汽车电动窗的组件来自动化他的滑动纱门。

在多余的部分从轨道上切下后，电机和轨道被安装在门框的顶部。一个长插销连接到轨道上的移动板上，推动门组件将其关闭。关闭后，该机构返回到其打开位置，允许门再次用手打开。电机由 Arduino 控制，运行一个非常简单的草图，它可以通过微动开关感应门是否关闭，并在门打开时开始 10 秒倒计时。两个继电器用于创建一个 H 桥电路，以双向驱动电机。

看起来没有任何检测是否被遮挡的规定。一个简单的解决办法是使推杆装有弹簧，这样，如果阻力过大，推杆可以滑过车门。

如果你只想让某些生物进入你的房子，我们不乏自动化宠物 T2 门 T3 供你享受。

 [https://www.youtube.com/embed/lGSw4oHZI04?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/lGSw4oHZI04?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

