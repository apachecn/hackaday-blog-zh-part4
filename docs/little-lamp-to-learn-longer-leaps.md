# 小灯学习更长的飞跃

> 原文：<https://hackaday.com/2019/05/25/little-lamp-to-learn-longer-leaps/>

强化学习是机器学习的一个子集，其中根据机器的性能对机器进行评分(“评估功能”)。在整个培训过程中，提高最终分数的行为会得到积极的强化，并逐渐朝着最佳解决方案发展。[Dheera Venkatraman]认为使用强化学习让一个小机器人灯移动会很有趣。但在此之前，他必须构建硬件，并用手动测试脚本证明其基本功能。

受皮克斯动画工作室跳跃标志的启发，这种特殊的运动形式在自然界中有一些对应的形式。但是自然界的蚱蜢不是 Luxo 灯的形状，这使得这个项目成为一个有趣的挑战。[Dheera]为这款 3D 打印灯发布了他所有的 OpenSCAD 文件，这样其他人也可以加入进来。灯头内部是一个 LED 环，用来照亮我们希望有灯泡的地方，同时也为摄像头留出了空间。机械关节伺服系统由 PCA9685 I2C PWM 驱动板驱动，他已经[编写并发布了代码](https://github.com/dheera/ros-pwm-pca9685)来将这些板与机器人操作系统(ROS)接口，以协调我们的灯的功能。这完成了该机器人灯的底层硬件组件和相关软件基础。

一旦所有的零件都被打印出来，电子线路连接好，所有的东西都组装好了，[Dheera]就拼凑了一个简单的“Hello World”脚本来验证他的机械设计已经足够好，可以开始使用了。休息后嵌入的视频是在奥什公园 2019 年 Maker Faire Bay Area 的 Bring-A-Hack afterparty 上拍摄的。这个动作序列是在 15 分钟内疯狂地手工编码的，但这些试探性的小跳跃将作为一个很好的基线。通过强化学习训练的控制算法的未来跳跃性能将显示这盏灯从这个不起眼的“Hello World”跳跃已经发展了多远。

[Dheera]之前已经创建了[影子时钟](https://hackaday.com/2019/03/20/an-esp8266-sundial-for-your-wall/)并且对 ROS 并不陌生，已经创建了 ROS 主题[文本可视化工具](https://hackaday.com/2019/03/31/ros-gets-quick-sensor-debugging-in-the-terminal/)用于调试。我们将拭目以待机器人 Luxo 将如何进化，希望它不会[找到作弊的方法](https://hackaday.com/2018/11/11/the-naughty-ais-that-gamed-the-system/)！想玩强化学习，却更喜欢轮式机器人？这里有几个选项。

 [https://www.youtube.com/embed/doaE-xDHTpM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/doaE-xDHTpM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

