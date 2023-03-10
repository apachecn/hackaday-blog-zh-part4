# 2022 年科幻竞赛:由 Arduino 驱动的手跟随机器人

> 原文：<https://hackaday.com/2022/04/13/2022-sci-fi-contest-a-hand-following-robot-powered-by-arduino/>

如果说科幻电影中有一件观众喜欢的东西，那就是一个可爱的机器人伴侣，它会跟随英雄们左右。如果你想要一个你自己的，从[mircemk]的这个版本开始[可能就是门票](https://hackaday.io/project/184681-diy-arduino-human-following-robot)。

该构建依赖于经典的 Arduino Uno 微控制器，该微控制器与 HC-SR04 超声波传感器模块和两个红外传感器对话，以便跟踪人类目标并跟随它。驱动是由于四个 DC 齿轮电机，由 L293D 电机驱动器驱动，双电池锂电池为船上的一切提供动力。

机器人以简单的方式工作，跟随放在机器人传感器前面的手。首先，机器人使用超声波传感器检查前方是否存在物体。如果检测到什么，安装在左右两侧的双红外传感器用来引导机器人跟随手。

这不是一个复杂的算法，它不会真的让你的机器人跟着你走在拥挤的街道上。然而，对于初学者来说，这是一个很好的学习项目，并且可以作为使用面部跟踪或其他技术的更高级项目的入门项目。休息后的视频。

 [https://www.youtube.com/embed/yNQKFEHJdYQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/yNQKFEHJdYQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[![Sci-Fi Contest](img/650ac107d73fa1ba67d57bd366e52230.png)](https://hackaday.io/contest/184314-sci-fi-contest)