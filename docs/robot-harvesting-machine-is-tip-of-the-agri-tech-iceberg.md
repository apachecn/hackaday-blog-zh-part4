# 机器人收割机是农业技术的冰山一角

> 原文：<https://hackaday.com/2019/07/09/robot-harvesting-machine-is-tip-of-the-agri-tech-iceberg/>

用机器人收割精致的水果和蔬菜很难，越来越多的美国人不再想做这些工作。寻找工程解决方案的压力很大，最近出现了越来越多不同形状和大小的机器，试图缓解这一问题。此外，每种作物通常彼此差异很大，因此，例如，草莓采摘机不能用于收获莴苣。

来自英国剑桥大学的一个团队最近[公布了他们的生菜采摘机](https://onlinelibrary.wiley.com/doi/full/10.1002/rob.21888)的细节，以一种漂亮易读的风格写成，并充满了有用的实用信息。非常值得一读！

![](img/f5a619d82de4e5196e9e07d8b7f83d9b.png)

该机器使用 YOLO3 检测和分类网络来获得作物的定位坐标，然后检查它是否可以收获，或者是否有病。然后，一个标准的 UR10 机械臂将收割机构放置在莴苣上方，通过机械臂关节获得力反馈，以检测它何时落地。然后，气动切割刀片试图在生菜头下方的正确高度切割生菜，以满足超市的严格要求。

相当奇怪的是，主要控制硬件只是一个标准的笔记本电脑，它处理 2 个消费级 USB 摄像头，总的组合检测和分类速度约为 0.212 秒。软件是 ROS(机器人操作系统)，带有团队成员用 Python 编写的自定义节点。

虽然这台机器速度慢，动力不足，但我们对它运转良好的事实印象深刻。这个特别的项目已经进行了几年，机器已经改造了 16 次！这些类型的机器目前(2019)还处于初级阶段，我们可以期待在未来几年看到更多尝试来解决这些困难的工程任务。

我们之前已经介绍过一些解决方案，包括:[除草机](https://hackaday.com/2018/05/18/autonomous-agribots-for-agriculture/)，一个自主农业机器人 [MoAgriS](https://hackaday.com/2018/05/14/moagris-a-modular-agriculture-system/) ，一个室内农业钻机[，一个激光发射鱼虱去除器](https://hackaday.com/2017/04/10/submersible-robots-hunt-lice-with-lasers/)，一个澳大利亚农业机器人，当然还有来自 FarmBot 的最新最棒的[。](https://hackaday.com/2019/07/01/farmbot-unveils-new-cnc-gardening-robot-models/)

休息后的视频:

 [https://www.youtube.com/embed/EFC3OvkVKaQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/EFC3OvkVKaQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

