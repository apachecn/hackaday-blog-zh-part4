# 霍尔效应模块知道你的马达在哪里

> 原文：<https://hackaday.com/2022/04/12/hall-effect-module-knows-where-your-motor-is/>

如果你有一个电机，你想知道轴的位置，你可能会转向光学编码器方案。然而，正如[lingib]指出的，你也可以使用[一个磁铁和一个磁力计](https://www.instructables.com/Magnetic-Shaft-Encoder/)。你可以在下面的视频中看到它是如何工作的。

MLX90393 是一种三轴霍尔效应器件，轴上有一个磁体，旋转磁体的 X 和 Y 输出将形成一个正交输出，您可以轻松读取。

磁铁足够强，地球的磁场变得可以忽略不计。后处理包括将两个输入缩放至相同幅度，并对其进行移位，使其以零为中心。那么以弧度表示的角度就是 X 和 Y 坐标的 atan2 函数。

我们总是对有多少种方法来测量任何一个特定的物理量感到兴趣。如果你想了解更多关于霍尔效应的知识，我们可以为你提供。除了磁性和光学，[机械编码器也很常见](https://hackaday.com/2018/02/19/roll-your-own-rotary-encoders/)。

 [https://www.youtube.com/embed/f3pePXkZ2gU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/f3pePXkZ2gU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

