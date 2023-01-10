# 蜘蛛机器人迈尔斯

> 原文：<https://hackaday.com/2020/08/06/miles-the-spider-robot/>

谁不爱机器蜘蛛？今天的仿生机器人以 [Miles 的形式出现，来自[_Robox]](https://www.instructables.com/id/Miles-a-Quadruped-Spider-Robot/) 的四足蜘蛛机器人。

Miles 使用 12 个伺服系统来控制它的运动，每条腿上有三个，还包括一个标准的 HC-SR04 超声波距离传感器，用于一些避障功能。12 个伺服系统可以使用相当多的功率，所以[_Robox_]必须用 6 个 LM7805 ICs 供电才能获得足够的电流。[_Robox_]激光切割了迈尔斯身体的丙烯酸片，但提到 3D 打印也可以工作。

迈尔斯使用反向运动学四处走动，[我们已经在之前的项目](https://hackaday.com/2020/07/03/robotic-biped-walks-on-inverse-kinematics/)中见过，这是一种[非常流行的控制机器人运动的技术](https://hackaday.com/2018/10/19/a-robotic-arm-for-those-who-like-their-kinematics-both-ways/)。Instructable 在细节上有点轻，[但是源代码是值得一看的](https://github.com/Robox-Robotics/Miles_the_spider_robot/blob/master/Miles_Sequence_code/Miles_Sequence_code.ino)。除了简单地走动[_Robox_]还开发了让 Miles 跳舞、挥手和鞠躬的代码。这肯定会在你的下一次虚拟展示中大受欢迎。

现在你在说“等等，蜘蛛有八条腿”，当然你是对的。但是那有很多伺服系统。无论如何，如果你宁愿 3D 打印你的四条腿的蜘蛛，[我们有一个建议。](https://hackaday.com/2017/04/22/hari-prints-an-awesome-spider-robot/)