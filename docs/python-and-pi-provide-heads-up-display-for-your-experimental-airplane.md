# Python 和 Pi 为你的实验飞机提供了平视显示

> 原文：<https://hackaday.com/2019/05/10/python-and-pi-provide-heads-up-display-for-your-experimental-airplane/>

你开车的时候不应该看着屏幕，但是抬头显示器呢？一个可以将相关信息放入你视野的屏幕会很棒，如果它使用树莓派就更好了。这正是约翰所做的，只不过他是用飞机做的。

首先，这个建筑的合法性。[约翰]的飞机被注册为实验性的，如果你知道你在做什么，这是非常接近于你想要的有人驾驶飞机的“任何事情”。[约翰]在他的日志上有足够的小时数，他建造了一个 Zenith 701。

对于硬件，这个构建的难点是构建一个平视显示器。幸运的是，售后 hud 是存在的，[约翰]正在使用一台 Kivic 投影仪，这是一台 200 美元的设备，在亚马逊上很容易买到。如果你的车需要一个 HUD，*这就对了。*软件完全是另一回事，目标是让软件与显示器和数据源分离。这在某种程度上很容易用树莓派来完成；该显示实际上只是 PyGame 内置的一些最小的基于文本的块状图形。这个构建还通过将它构建为 [Stratux](http://stratux.me/) 的用户界面来与数据源解耦，Stratux 是一个独立的基于 Raspberry Pi 的飞行员 ADS-B 接收器。

这个 HUD 有几个可用的视图，AHRS + ADS-B 提供飞机姿态和高度的信息，以及最近飞机的几个指示器。交通视图扩展了 ADS-B 数据，显示了空中最近的八架左右的飞机，以及距离、方位和高度差。有一个诊断窗口，因为[约翰]的飞机是一个穷乡僻壤的 STOL 东西，可以在强风中悬停，也有一个诺顿投弹瞄准器的数字版本。这是用来把一袋袋面粉扔到草坪上的。你可以在下面查看[John]的整个 AirVenture 演示，这里有[所有可用的代码](https://github.com/JohnMarzulli/StratuxHud)。

 [https://www.youtube.com/embed/Du7jkJTLTPo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Du7jkJTLTPo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

