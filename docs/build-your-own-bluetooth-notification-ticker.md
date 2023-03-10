# 构建您自己的蓝牙通知跑马灯

> 原文：<https://hackaday.com/2021/04/21/build-your-own-bluetooth-notification-ticker/>

股票行情自动收录器是 19 世纪基于电报的机器，随着 20 世纪 60 年代以来计算机替代品的出现，它很快就被抛弃了。然而，向我们传递纸条信息的小型机器也有一些迷人之处——[来自【DIY projects】](https://m.habr.com/en/post/407057/)(俄语，[谷歌翻译链接](https://translate.google.com/translate?hl=&sl=ru&tl=en&u=https%3A%2F%2Fm.habr.com%2Fen%2Fpost%2F407057%2F))的通知信息显示了这一点。

构建的核心是 Arduino Mini，它通过连接到其串行端口的蓝牙模块接收智能手机通知的文本内容。该机器安装了一个小纸卷，由一个装有橡胶耳塞的步进电机拖动，以增加抓地力。使用 Lambda 机制的伺服系统使笔沿着纸张移动，以使其垂直于纸张的行进方向移动。不是上下移动笔，而是通过安装在下方的螺线管将纸推入笔中。

这是一个有趣的小项目，我们可以想象这是一个伟大的教育项目。它教授与步进器、伺服系统、螺线管和蓝牙一起工作所需的技能。[它与其他一些笔式绘图仪的设计有些不同，](https://hackaday.com/2020/05/23/conduit-birdhouse-and-skateboard-become-giant-pen-plotter/)但是 ticker 格式有一种其他方式很难复制的魅力。休息后的视频。

 [https://www.youtube.com/embed/MVHfoNOy69I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/MVHfoNOy69I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



【感谢 Baldpower 的提示！]