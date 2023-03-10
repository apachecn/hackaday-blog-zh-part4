# 感谢谷歌人工智能的 3D 动画

> 原文：<https://hackaday.com/2021/04/15/3d-animation-for-all-thanks-to-google-ai/>

谷歌很少不通过技术演示给人留下深刻印象。他们的最新产品——Monster Mash——旨在使用人工智能来创建简单的 3D 动画，而无需大量培训或麻烦。我们要警告你:我们不是艺术家，所以我们没有得到演示显示的结果，但话说回来，如果你甚至有点艺术感，你可能会比我们运气好。你可能想开始看下面的视频。

如果你对这项技术更感兴趣，还有一篇研究论文。这个想法是在 2D 画简单的线条画。然后你把物体膨胀成 3D。最后一步是描绘出动画路径。

这听起来很简单，但有几件事你需要知道。对象的主体需要是封闭的笔画。之后，您可以绘制开放的形状来提示系统它们是身体部位。右键单击绘图会将对象放在现有对象的后面，双击形状会创建一个对称的副本(例如，左右腿)。膨胀步骤背后有一些高功率数学，而最后一步是在模型上创建控制点，并使它们变形以产生运动的外观。

该项目的参与者来自捷克技术大学、苏黎世联邦理工学院和华盛顿大学。代码也是[开源](https://github.com/google/monster-mash)。

 [https://www.youtube.com/embed/LbjF-MylQzk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=2&wmode=transparent](https://www.youtube.com/embed/LbjF-MylQzk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=2&wmode=transparent)

