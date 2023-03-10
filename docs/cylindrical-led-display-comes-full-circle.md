# 圆柱形 LED 显示屏绕了一圈

> 原文：<https://hackaday.com/2019/03/05/cylindrical-led-display-comes-full-circle/>

根据[makeTVee]的说法，他的最新项目是从一个实验开始的，以观察他过去使用的 LED 矩阵技术如何转化为圆柱形形状因子。我们将继续说，不仅测试是成功的，而且这一概念肯定为兼具功能和美感的显示器带来了希望。这个构建离一个完整的实现还差一点，但是他目前所做的非常有前途，我们希望他继续充实它。

[![](img/9b7073a82f75ebbaa8f93f892bc877ec.png)](https://hackaday.com/wp-content/uploads/2019/02/ledcyl_detail.jpg) 激光切割机被用来制作组成显示器框架的互锁部分，但我们想象如果你没有激光，你可以使用 3D 打印部件完成类似的设计。WS2812 LEDs 灯条沿圆柱体内部安装，使每个单独的 LED 灯与电池中心对齐。为了完成圆柱体的外部,[makeTVee]使用了一种叫做 MicroWOOD 的薄木皮，它给 led 提供了一种良好的漫射光。单板中的木纹也提供了一种有机的触感，使整体看起来不会太单调。

当然，像这样的显示器只有在你有软件驱动的情况下才能工作。为此，[makeTVee]已经使用 pygame 在他的电脑上创建了一个模拟器，展示了如果显示器被展开并展平时的样子。这使得创建内容更加容易，因为您可以一次看到整个显示。他说新工具的源代码很快就会出现在 GitHub 上，我们非常有兴趣看一看。

如果这个显示器看起来很熟悉，那可能是因为[它的一个明显更平的版本在我们去年的“用圆周率可视化它”比赛中获得了冠军](https://hackaday.com/2018/10/12/contest-results-raspberry-pis-put-on-a-show/)。

 [https://www.youtube.com/embed/2VNS9aFNEW0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/2VNS9aFNEW0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

