# 麻瓜用电子纸复制每日先知

> 原文：<https://hackaday.com/2021/10/29/muggle-uses-e-paper-for-daily-prophet-replica/>

对于普通麻瓜来说，来自魔法世界的消息有点难以获得，但是[Deep Tronix]通过他们的《预言家日报》的电子副本让我们离我们的魔法同行更近了一步。

熟悉《哈利·波特》系列的人无疑会熟悉《预言家日报》。在电影中，报纸以其怪异的动画形象特别引人注目，反映了魔法世界的现状。这是通过电影的后期制作特效实现的，但这个粉丝制作的先知首页使用电子纸技术和其他一些有趣的小工具将这个概念带入生活，所有这些都隐藏在一个相框中。

如上所述，这个项目的核心是电子纸显示器和一个微型控制器。虽然电子纸显示器非常适合显示静态文本和简单的图形，但它们通常不适合移动图像，因为它们会遭受某种形式的“烧屏”,这会在屏幕上留下错误的像素。这意味着电子纸技术通常具有相对较低的视频帧率。[Deep Tronix]使用了一个自定义抖动库来缓解这个问题，结果令人印象深刻。运动图像从外部 SD 卡加载，经过处理，然后显示在电子纸显示器上，与周围的报纸印刷品几乎无法区分。

这份看似神奇的报纸还具有人脸检测功能，这是由隐藏的摄像头和古老的 ESP32 微控制器实现的。该系统与 Teensy 集成，记录并在电子纸显示器上显示读者的面部。这是一个巧妙的把戏，当这些面孔随后被随机展示时，这变得更加诡异。

[在](https://hackaday.com/2017/07/03/daily-prophet-is-a-magic-newspaper-kinda/)之前，我们已经看到了使用更传统显示技术的《预言家日报》复制品，然而，尽管帧率较低，但转向电子纸显示对提高整体美观有很大帮助。随着万圣节即将来临，你可能最终会用这个聪明的道具欺骗一些人——[点击这里查看所有的建造细节](https://deeptronix.wordpress.com/2020/09/02/a-proper-harry-potter-newspaper-irl/)。

 [https://www.youtube.com/embed/ZxRA6Q5PZA8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ZxRA6Q5PZA8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

