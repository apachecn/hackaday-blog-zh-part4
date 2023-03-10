# 循线机器人使用 PID 控制速度

> 原文：<https://hackaday.com/2021/09/18/line-following-robot-uses-pid-for-speed/>

虽然循线机器人可能不是书中最新的项目想法，但来自[爱迪生科学]的这个机器人是使用现代组件的[全新构建，并由于 PID 控制反馈而不是低端机器人中更传统的 bang-bang 控制而获得了良好的速度。](https://www.youtube.com/watch?v=bZJYAhzlYa0)

当然，PID 需要调整，这似乎是薄弱环节——您必须对设置进行试验。传感器也需要校准，但我们打赌这两个问题都很容易解决。

如果 PID 的概念对你来说是新的，缩写代表比例，积分和微分。要确定在任何给定时间的产量，你需要将你的产量与你想要的产量进行比较(现值与设定值)。然后你计算一个比例误差。例如，对于一个温度，如果你想在 30 度，而你在 20 度，那么比例误差为 10 度。您还希望了解随着时间的推移已经积累了多少变化，以及误差的变化率。

如果你想读点数学，我们过去有一些很棒的 PID 教程。蒂耶最简单的线追随者[不需要 PID](https://hackaday.com/2017/03/18/line-follower-has-lots-of-recycled-parts-but-zero-brains/)甚至 CPU。

 [https://www.youtube.com/embed/bZJYAhzlYa0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/bZJYAhzlYa0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

