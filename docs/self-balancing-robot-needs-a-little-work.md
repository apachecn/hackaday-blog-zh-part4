# 自平衡机器人需要一点工作

> 原文：<https://hackaday.com/2021/09/20/self-balancing-robot-needs-a-little-work/>

自平衡机器人并不是一个新想法，但我们喜欢[制造商 ATOM 的[建造](https://www.instructables.com/The-Breadboarded-Self-Balancing-Robot/)的美学。使用试验板和印刷支架看起来不错，正如你在下面的视频中看到的那样。

像大多数第一次的项目一样，也有一些经验教训。电源需要稍加改进，平衡合规性范围未达到预期。但是这些问题是可以解决的，通常，你会从解决这些问题中学到更多。

该系统的核心是一个 MPU6050，它提供陀螺仪和加速度计以及板上融合功能。传感器和 PID 控制器库的可用性使得这个项目很容易完成。

具体来说，PID 控制回路着眼于系统的期望状态和当前状态。然后，它以不同的方式基于当前时间和一段时间内的状态差异来计算输出。换句话说，输出的一部分是由于原始差异形成的，而输出的其他部分是由于随时间累积的误差或突然的扰动形成的。调整增益使这些部分保持平衡可能有点棘手。

然而，最终，两块电池不足以给设备提供充足的电力。暂时，一个工作台电源完成了这个任务，但是电池仍然需要在那里提供一些平衡配重。尝试一些 PID 环路增益也可能改善操作。

有很多类似的项目可以从中汲取灵感。设计[不一定很难](https://hackaday.com/2017/06/03/building-a-self-balancing-robot-made-easy/)。

 [https://www.youtube.com/embed/w0-hJJNbFuY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/w0-hJJNbFuY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

