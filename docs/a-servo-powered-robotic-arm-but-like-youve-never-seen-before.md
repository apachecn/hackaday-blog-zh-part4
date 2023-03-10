# 一个伺服驱动的机械手臂，但是你从来没有见过

> 原文：<https://hackaday.com/2018/09/04/a-servo-powered-robotic-arm-but-like-youve-never-seen-before/>

我们已经写了很多 DIY 机械臂。有些是高性能的，有些是廉价的，有些只是独特的乐趣。这个肯定属于最后一类；在观看《黑镜》的一集时，一个细长的机器人肢体给了我灵感。经过一些迭代之后，他有了最终的原型，而且[在行动中](https://www.youtube.com/watch?v=qihjxvOIFr0)很值得一看。

为了使机械臂尽可能细长，致动器不能安装在机械臂上，而是必须远程驱动机械臂。有很多方法可以做到这一点，虽然[齿轮下来]考虑使用气动或液压，他选择保持简单的钢筋混凝土伺服产生一个漂亮的解决方案，我们真的很喜欢。

该手臂由一系列 3D 打印的球形接头制成，允许向任何方向旋转。棘手的是将伺服系统的力传递到每个关节。最初考虑的是裸露的钓鱼线，但这使得当下部关节移动时，远程关节难以控制。解决方案是使用油管内的钓鱼线，类似于自行车刹车的操作方式。这允许力被传递到适当的关节，而不管较低的运动。每个关节需要一个 x 和 y 张力来允许它向任何方向旋转，这意味着需要 16 个伺服系统来操作八段臂。

建造机器人手臂总是很有趣，我们已经看到了它们的一些非常巧妙的用途，例如[绘制 3D 磁场图](https://hackaday.com/2014/03/30/measuring-magnetic-fields-with-a-robotic-arm/)，或者[教授手语](https://hackaday.com/2017/08/24/3d-printed-robotic-arms-for-sign-language/)。

 [https://www.youtube.com/embed/qihjxvOIFr0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/qihjxvOIFr0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

