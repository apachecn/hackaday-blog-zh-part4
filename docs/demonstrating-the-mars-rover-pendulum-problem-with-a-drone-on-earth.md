# 在地球上用无人驾驶飞机演示火星漫游车钟摆问题

> 原文：<https://hackaday.com/2021/02/25/demonstrating-the-mars-rover-pendulum-problem-with-a-drone-on-earth/>

毅力号和好奇号火星车上使用的天空起重机系统是一个具有挑战性的控制系统问题，激起了[尼古拉斯·雷姆]的好奇心。由于被困在地球上，他决定用一架无人机和一块石头来调查这个问题。

设置和测试很简单，但清楚地说明了美国宇航局工程师面临的问题。[尼古拉斯]在赛车型四轴飞行器的底部安装了一个绞盘装置，并在绞盘线的末端绑了一个重物。起初，他建造了一个火星车的泡沫模型，但事实证明它在四轴飞行器的螺旋桨尾流中不稳定，所以他用一块石头代替。测试从四轴飞行器起飞开始，岩石完全缩回，然后在飞行中慢慢下降，直到它到达线的末端并自由下落。一旦岩石被放下，它就开始像钟摆一样摇摆，随着钓线变长，这种情况只会变得更糟。[Nicholas]试图通过手动控制输入来减少振荡，但这只会使情况变得更糟。四轴飞行器还运行着【尼古拉斯】自己的 [dRehmFlight](https://hackaday.com/2021/02/15/drehmflight-customizable-flight-stabilisation-for-your-weird-flying-contraptions/) 飞行控制器，该控制器处理稳定，但它不考虑摇摆质量。

[Nicholas]详细介绍了这个系统的动力学，它基本上是一个两体钟摆。精确控制两体钟摆的挑战是天空起重机概念在 1999 年首次提出时被搁置的主要原因之一。无人机或岩石的任何水平运动都会对另一个物体施加力，并将导致钟摆运动开始，如果不考虑这一点，控制系统将无法恢复。真正的天空起重机可能在系绳上有某种角度感应，可以用来补偿悬浮漫游车的任何运动。

我们希望[Nicholas]能够继续这个实验，展示如何使用他的[dRehmFlight](https://hackaday.io/project/174768-drehmflight-vtol)飞行控制器来解决这个问题。dRehmflight 的可定制性应该使它成为这项工作的完美工具

一定要看看[丹·马洛尼]在“坚持”着陆程序的“[七分钟恐怖](https://hackaday.com/2021/02/08/getting-ready-for-mars-the-seven-minutes-of-terror/)中的深潜，当然还有成功着陆的[令人难以置信的视频。](https://hackaday.com/2021/02/22/stunning-footage-of-perseverance-landing-on-mars/#more-463767)

 [https://www.youtube.com/embed/6KsFICAE1vE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/6KsFICAE1vE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

