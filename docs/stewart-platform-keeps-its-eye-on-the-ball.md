# 斯图尔特平台关注着球

> 原文：<https://hackaday.com/2023/01/04/stewart-platform-keeps-its-eye-on-the-ball/>

虽然号称是一个平衡机器人，但[Aaed Musa 的]机器人不会自己平衡。它[在平台](https://www.instructables.com/Ball-Balancing-Robot/)上平衡一个球。你可能会认为这是一个叫做 Stewart platform 的东西，如果你碰巧和一群热爱自动化的黑客在一起，他们在聚会上会很有趣。看看下面的视频，看看该设备的行动。

如果你想复制这个项目，会有一点费用，但视频中解释了背后的想法。机器人的大部分都是 3D 打印的，带有螺纹插件。甚至连球都是 3D 打印的，分为两部分，还有一个立方体连接器将两个半球连接在一起。丙烯酸平台是用水射流切割的，尽管你也可以用手工工具轻松切割。

这种类型的机器人是 PID 控制的一种特别的视觉表现，这在第二个视频中有解释。当然，大多数 3D 打印机使用它来控制喷嘴温度，但这几乎没有看着球在平台上滚动那么令人兴奋。

该算法的关键是认识到你必须同时控制球的位置和速度。你希望球到达设定点——平台的中间——就像它的速度变为零一样。这意味着算法必须调整平台倾斜的方向以改变球的运动方向，还必须调整倾斜的程度以控制速度。

出于某种原因，我们最近看到了更多的 Stewart 平台。其中一些有非常现代的外观。

 [https://www.youtube.com/embed/kAaYaZcpbLo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/kAaYaZcpbLo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/NwRuQ7r6xLQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/NwRuQ7r6xLQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

