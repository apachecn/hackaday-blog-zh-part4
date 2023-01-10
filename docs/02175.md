# 自行车的防抱死刹车可能会让骑行更安全一点

> 原文：<https://hackaday.com/2019/02/17/anti-lock-brakes-for-bike-might-make-rides-a-little-safer/>

撞毁一个人的自行车是一个童年的成年礼，可以在应用物理学中教授有价值的课程。假设孩子得到了适当的保护，车祸相当温和，擦伤和瘀伤换来了避免沙子和砾石的智慧，以及如何通过不要比后刹车更用力地施加前刹车来避免弹道式坠落。

但对我们中的许多人来说，这些教训是很久以前用比我们现在更灵活的身体学到的，对于包括刹车失误的自行车骑行来说，风险更高。为了帮助解决这个问题，[汤姆·斯坦顿]一直在研究自行车的防抱死刹车，在这个过程中，他学到了很多关于可控减速的物理学和工程学知识。

这似乎是一个简单的概念——使用传感器来检测车轮何时因轮胎和路面之间的摩擦减少而打滑，并通过执行器反复释放制动力，让驾驶员或骑手在停车时保持控制。但这抽象掉了大量的细节，而[汤姆]很快就陷入了困境。前轮上有一个光电传感器和一个步进电机来超越刹车杆的输入，他能够调节制动力，但没有保持控制所需的响应能力。几次迭代之后，[Tom]找到了传感器、致动器和算法的正确组合，来制作一个像样的自行车 ABS 系统。下面的视频包含了构建和测试的所有细节。

[Tom]承认自行车 ABS 不是什么创新。我们甚至报道了几年前作为 ABS 测试平台的 Arduino 自行车。但是看到防抱死系统的投入还是很酷的。

 [https://www.youtube.com/embed/iiRpGHiKHJ0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/iiRpGHiKHJ0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

