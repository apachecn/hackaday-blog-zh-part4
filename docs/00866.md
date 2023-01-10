# 单腿跳跃机器人表明控制就是一切

> 原文：<https://hackaday.com/2018/10/09/one-legged-jumping-robot-shows-that-control-is-everything/>

会跳的机器人以前也见过，但是一个一直跳*的机器人*就有点不一样了。Salto-1P 是加州大学伯克利分校的一个单腿跳跃机器人，早在 2017 年，它就展示了通过足够的控制来保持平衡的连续跳跃能力。从那以后，它学会了一些新的技巧；已经超越了基本的稳定性，它现在可以[以令人印象深刻的控制程度在东西上跳跃](https://spectrum.ieee.org/automaton/robotics/robotics-hardware/jumping-robot-salto1p)。

做到这一点的关键是能够将它的单脚准确地放在它想放的地方，这允许更复杂的行为，例如跳上或跨越不同的物体。[Justin Yim]在下面嵌入的视频中展示了这一点，该视频演示了 Salto-1P 以非常可控的方式反弹，即使在倾斜的表面等非理想物体上也是如此。两个小螺旋桨可以让机器人在半空中扭动，但所有的动力都来自单腿。

 [https://www.youtube.com/embed/ZFGxnF9SqDE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ZFGxnF9SqDE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



挑战的一部分在于，对机器人的下一步行动施加任何真正控制的唯一机会是在脚真正接触地面的那一小段时间里。在那之后，就只是物理表演了。运动规划的大部分工作都是在动作捕捉的帮助下完成的，但研究人员正在努力改进更多的东西，不再需要这种外部依赖。

如果一台机器不需要控制它去哪里，它甚至可以只用一个马达而不用像 [*奔跑者*](https://hackaday.com/2016/08/06/simplest-jumping-kangaroo-bot/) 那样的传感器。我们甚至看到[一个轮式机器人证明跳跃不需要腿](https://hackaday.com/2010/06/25/jumping-robot-looks-like-a-product-of-doctor-wily/)。