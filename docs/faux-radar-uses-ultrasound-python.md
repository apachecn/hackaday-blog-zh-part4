# 人造雷达使用超声波和 Python

> 原文：<https://hackaday.com/2020/07/18/faux-radar-uses-ultrasound-python/>

雷达很酷，在电影和电视中的表现与此有很大关系。你得到一个可爱的发光屏幕，显示你在哪里的坏人，和一个可视化的代表你的导弹在途中炸毁他们。可悲的是，或者也许值得庆幸的是，对我们大多数人来说，日复一日的生活并不那么令人愉快。[我们可以用体验的复制品来代替。](https://makersportal.com/blog/2020/3/26/arduino-raspberry-pi-radar)

该项目包括一个配备超声波模块的 Arduino Uno，可以进行几十厘米的基本距离测量。该模块然后被放置在一个伺服和扫描通过 180 度旋转。这些数据被传回运行 Python 应用程序的计算机，该计算机将结果绘制在平面位置指示器(PPI)上，这是我们都非常熟悉的扫描显示。

虽然你不太可能使用这样的设置来对付强盗，但它可以证明是机器人导航或类似应用的有用模块。我们已经看到超声波传感器正是用于这一目的。休息后的视频。

 [https://www.youtube.com/embed/M7A81Yh7PSM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/M7A81Yh7PSM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

