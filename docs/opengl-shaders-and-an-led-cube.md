# OpenGL 着色器和 LED 立方体

> 原文：<https://hackaday.com/2019/04/30/opengl-shaders-and-an-led-cube/>

今年 2 月，在荷兰的 Hacker Hotel camp，会场周围的许多作品中有一个相当吸引人的 LED 立方体。很漂亮，但是 LED 立方体以前做过很多次了。

如果一个不经意的参与者花时间问一下，他们可能会发现一些更有趣的东西，因为尽管有问题的立方体可能和其他立方体有相同的硬件，但它肯定没有相同的软件。[poly loyd]为他的 LED 立方体配备了 OpenGL 着色器，以将任意图像映射到 3D 空间中的立方体像素。

硬件方面，它与其他立方体使用的全球速卖通 LED 面板和 Raspberry Pi 驱动板的集合相同，在这种情况下，安装在定制的激光切割框架上。驱动软件来自于[一个开源库](https://github.com/hzeller/rpi-rgb-led-matrix)，他在库的周围[放了一个允许通过 UNIX 管道输入的包装器](https://github.com/hzeller/rpi-rgb-led-matrix/blob/master/examples-api-use/ledcat.cc)。这可以采用 OpenGL 着色器的 RGB 输出，他已经创建了 2D 到 3D 和球形投影版本。必看的演示是全球光污染地图，结果是一件相当令人印象深刻的作品。

如果你喜欢 LED 立方体，别忘了最近的 Hackaday 奖参赛作品。