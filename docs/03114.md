# 一条腿的机器人会跳

> 原文：<https://hackaday.com/2019/05/25/one-legged-robot-does-the-hop/>

起初，我们认为这个机器人像一只兔子，直到我们意识到兔子在腿部有 300%的奖金。[SALTO](https://people.eecs.berkeley.edu/~ronf/PAPERS/jyim-icra2019.pdf)——来自【贾斯汀·延】、【王传君】和【罗纳德·费林】的一个机器人只有一条腿，但却能很好地从一个地方跳到另一个地方。如果你无法描绘出来，下面的视频会让它变得非常明显。

根据这篇关于 SALTO 的论文，现有的跳跃机器人需要外部传感器，并且通常被拴着。萨尔托自成体系。这个机器人重十分之一公斤，它的名字来自单词 saltatorial(适于跳跃),这个单词本身来自拉丁文 *saltare* ,意思是跳跃。

机器人认为自己有四种不同的模式:站姿是当它站在地面上时，升空是当它发射自己时，飞行是在空中，触地是当它与地面重新连接时。当然，在站立时保持机器人的平衡已经过时了。但是在起飞时，机器人会计算出速度的误差项，并用它来计算修正值。机器人有一条尾巴和两个小螺旋桨来控制它的姿态。

开始时，机器人在三个点上保持平衡:脚趾、后脚踝和尾巴的一端。使用陀螺仪，它能够设置初始值。然后，它以不同的姿势站立起来，并使用推进器消除任何滚动和俯仰。

在我们怀疑小动物是否会爬楼梯之前，我们还没看多远。它不能。根据作者所说，估计误差意味着脚可以移动到离你想要它落地的地方半米远的地方。然而，他们相信未来的版本将会提高估计能力，让它能够爬楼梯，跳过家具或其他障碍物，并处理各种地形。我们只希望他们能把这个可怜的东西打印成袋鼠的身体。

跳跃机器人总是让我们回想起 [Atlas](https://hackaday.com/2018/10/13/atlas-is-back-with-some-new-moves/) 撞开卧室门的噩梦。他对楼梯没有问题。我们还看到了一辆[原型月球车](https://hackaday.com/2019/05/15/2019-cornell-cup-winners-include-autonomous-boat-flapping-uav-and-leaping-rover/)，它可以跳过东西，尽管这不是它的主要移动方式。

 [https://www.youtube.com/embed/hy2XTDMr0co?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/hy2XTDMr0co?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/qFmeHPVtK0o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/qFmeHPVtK0o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

