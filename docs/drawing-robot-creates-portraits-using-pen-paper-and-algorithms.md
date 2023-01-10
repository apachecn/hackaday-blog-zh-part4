# 绘图机器人使用笔、纸和算法创建肖像

> 原文：<https://hackaday.com/2021/10/25/drawing-robot-creates-portraits-using-pen-paper-and-algorithms/>

尽管随着摄影技术的发明，手绘肖像的市场在很大程度上崩溃了，但是看着一个艺术家只用一支铅笔、一些纸和他们精细的动作技巧创造出栩栩如生的图像，还是有一种神奇的感觉。看着一台机器做同样的事情也是一种同样迷人的体验，尽管通常最终结果并不那么好。为了弥补这一缺陷，[Joris Wegner]和[Felix figus]创造了[Pankraz Piktograph](https://felixfisgus.de/work/017_pankraz_piktograph)，它似乎在捕捉人脸方面做得很好。他们受到经典绘画机器人的启发，制作了一个 21 世纪的版本，用于博物馆或贸易展览等活动。

Piktograph 的操作非常简单:你站在机器前面，看着相机自拍。如果你喜欢你所看到的，机器人就会开始在一张纸上画出你的肖像。它使用两个由铝制成、由两个步进电机驱动的类似人类的手臂来实现这一点。一只普通的圆珠笔放在一个装有弹簧的托架中，它提供了足够的笔到纸的压力来可靠地画线，而不会提离或刮伤纸张。我们不禁对这台机器的整体外观印象深刻:光滑的粉末涂层铝外壳和不锈钢支架本身就是一件艺术品。

在内部，Piktograph 由 Raspberry Pi 3 驱动，它运行一个相当复杂的算法来生成一个矢量图像，这个图像不会花太长时间来绘制，但仍然会产生一个可识别的主题图像。制作者的[论文](https://felixfisgus.de/user/downloads/Masterthesis_JW_FF.pdf)相当详细地解释了这个过程，它使用 [Canny 边缘检测](https://en.wikipedia.org/wiki/Canny_edge_detector)来创建一个轮廓图，然后填充空白处来创建明亮和黑暗的区域。将一定量的噪波和扭曲添加到线条中，使其更有“手工”的感觉，并且生成的图形被划分为连续的线条，以便绘图仪高效地绘制。

我们以前见过几种类型的专业艺术机器人，能够用钢笔[画肖像](https://hackaday.com/2021/04/05/arduino-plots-your-portrait-with-style/)，[画肖像](https://hackaday.com/2019/10/11/portrait-painter-turns-g-code-into-artworks/)，甚至[用蚀刻素描](https://hackaday.com/2019/07/30/etch-a-selfie/)，但是【乔里斯】和【费利克斯】的创造似乎在速度、做工和最终结果的质量上胜出。休息后嵌入的视频。

[https://player.vimeo.com/video/620658641](https://player.vimeo.com/video/620658641)