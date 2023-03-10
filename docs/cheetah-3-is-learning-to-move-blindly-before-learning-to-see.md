# 猎豹 3 号在学会看之前正在学习盲动

> 原文：<https://hackaday.com/2018/07/11/cheetah-3-is-learning-to-move-blindly-before-learning-to-see/>

马上站起来，四处走走。我们很确定你没有看到你走过的每一个地方，也没有根据视觉输入精心计划每一步。那么为什么机器人也要这样做呢？如果你的机器人可以利用视觉规划路径，但借助各种传感器和关节位置的知识，将大部分行走任务留给腿，那不是更通用吗？

这就是[金相培]和麻省理工学院的一组研究人员在他们的猎豹 3 上采用的方法。他们给了它摄像头，但还没有使用。相反，[他们首先要确保它能在没有遮挡的情况下四处移动](http://news.mit.edu/2018/blind-cheetah-robot-climb-stairs-obstacles-disaster-zones-0705)。到目前为止，他们已经学会了走路、跑步、跳跃，甚至爬楼梯，上面堆满了松散的积木和胶带卷。

![Cheetah 3 jumping 30 inches onto a desk](img/0b232b37ba302ae0bae2583404c6bae8.png)

Jumping 30 inches onto a desk

两种算法是它能够盲目移动的核心。

第一个是接触检测算法，该算法基于关节位置的知识和来自陀螺仪和加速度计的数据来决定腿是否应该在摆动或迈步之间转换。如果它由于踩在一块松动的石头上而意外倾斜，那么这就是决定腿应该做什么的算法。

第二种是模型预测算法。这预测了一旦决定迈出一步，一条腿应该施加多大的力。它通过计算半秒钟后机器人身体和腿的乘法位置来做到这一点。这些计算每秒钟进行 20 次。它们帮助它处理各种情况，比如有人推它或用皮带拉它。这些计算使它恢复了平衡，或者继续朝着它前进的方向前进。

这个四足机器人还有许多其他令人敬畏的功能，这些功能我们在其他产品中没有见过，如波士顿动力公司的 SpotMini，如可翻转的膝关节和三条腿行走。在下面的视频中查看这些功能和更多内容。

当然， [SpotMini 有一整套自己的整洁功能](https://hackaday.com/2016/07/01/spotmini-struts-its-stuff/)。这么说吧，虽然它们看起来非常相似，但它们走在两条不同的进化道路上。自从几年前我们最后一次看到猎豹以来，猎豹确实已经进化了[。](https://hackaday.com/2014/09/15/mits-robotic-cheetah-is-getting-even-scarier/)

 [https://www.youtube.com/embed/QZ1DaQgg3lE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/QZ1DaQgg3lE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



我们感谢[Qes]发送了这条提示。