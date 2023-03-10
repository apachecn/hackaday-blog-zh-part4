# Rollbot 在一个轮子上塞入十只手臂

> 原文：<https://hackaday.com/2020/02/06/rollbot-crams-ten-arms-onto-one-wheel/>

我们并不是每天都能看到有人尝试机器人运动的新东西，但是[kong]的机器人 [Rollyboi 通过混合通常的机器人-轮子-马达布局来完成这一任务](https://www.robotshop.com/community/robots/show/rollbot)。Rollyboi 不是机器人使用电机来驱动轮子，而是它本身就是轮子，使用多个简单的手臂(腿？)连接到业余爱好伺服电机来推进自己。这个想法是，手臂一次向外旋转一个，根据需要滚动机器人。

这是一个新奇的想法，但在实践中它能发挥多大作用呢？第一个版本是盲目的，机械上不稳定，不知道哪个方向是向上的，因此没有办法有效地控制哪个手臂需要伸出，但仍然能够滚动。下一个版本实现了一个简单的控制系统:安装在外部边缘的按钮让机器人知道它如何移动以及下一步该伸出哪只手臂。有了两组手臂(一边一个)，机器人就能够通过将一个手臂伸出比另一个手臂更多来执行简单的转弯。

最终，Rollyboi 可以移动，但仍然缺乏感知和导航环境的方法。随着机器人的移动，机器人的身体(以及安装在其上的任何传感器)将处于不断的运动中，这使得这更具挑战性。不过，有趣的是看到这个想法只用简单的硬件走了多远，它的运动发出某种[径向螺线管发动机振动](https://hackaday.com/2016/05/20/scratch-built-radial-solenoid-engine-is-polished-and-professional/)。可以看下面一个简短的视频。

 [https://www.youtube.com/embed/pHYDl1TK4sk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/pHYDl1TK4sk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

