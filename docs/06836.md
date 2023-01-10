# 无人机避障，从蚊子那里学来的

> 原文：<https://hackaday.com/2020/06/17/obstacle-avoidance-for-drones-learned-from-mosquitoes/>

我们对动物感官能力的了解有很多空白，而新的发现往往会成为新技术的灵感。利兹大学和皇家兽医学院的研究人员发现，蚊子可以在完全黑暗的情况下通过探测当它们飞近障碍物时产生的气流的微妙变化来导航。然后，他们利用这一知识建立了一个简单而有效的传感器，用于无人机。

蚊子头部触角底部极其敏感的感受器被称为约翰斯顿器官，允许它们感知气流中的这些微小变化。使用基于高速摄影的流体动力学模拟，研究人员发现，气流的最大变化发生在蚊子的头部，这意味着感受器处于完全正确的位置。根据他们的数据，科学家们预测蚊子可能在超过 20 个翅膀长度的距离探测表面。考虑到 20 臂长对我们来说有多远，这已经很了不起了。如果你能通过付费墙，你可以阅读科学杂志上的[全文](https://science.sciencemag.org/content/368/6491/634)。

利用他们新发现的知识，研究人员为一架小型无人机配备了连接到压差传感器的探测管。使用这些传感器，无人机能够有效地检测何时接近墙壁或地板，并避免碰撞。传感器还需要很少的计算能力，因为它只是一个基本的阈值。休息之后请看视频。

虽然这种传感方法可能不会取代无人机的超声波或飞行时间传感器，但它确实表明我们仍然可以从大自然中学习很多东西，而且越简单越好。我们已经看到了简单的昆虫启发的无人机群导航，以及用于人类的[光学导航设备](https://hackaday.com/2019/09/06/building-a-gps-with-bug-eyes-and-ancient-wisdom/)，它没有卫星也能工作，只需要一个天空视图。谢谢你的提示！

 [https://www.youtube.com/embed/AIpzxEK6xm4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/AIpzxEK6xm4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[https://tech xplore . com/news/2020-05-蚊子-四轴飞行器-夜晚. html](https://techxplore.com/news/2020-05-mosquitoes-quadcopters-night.html)