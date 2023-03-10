# 又一个机器人魔方解算器

> 原文：<https://hackaday.com/2019/06/03/yet-another-robotic-rubiks-solver/>

《魔方》在 1974 年问世时大受欢迎，并一直持续到今天。这可能很难解决，但许多人接受了挑战。Arduino Rubik's Solver 是一个使用电子和数学来完成工作的机器人。

该系统由基于计算机的软件和硬件系统协同工作来解决立方体。网络摄像头的图像在计算机上处理，确定立方体的当前状态，以及解决它所需的必要动作。解算装备由钢棒、激光切割丙烯酸树脂和 3D 打印部件构成，还有一个 Arduino 和六个步进电机。Arduino 通过 USB 串行链路接收来自解算计算机的指令。这些然后被用来命令步进电机以正确的方式操纵立方体。

它不是速度恶魔，但这个装置能够毫无问题地解决一个立方体。立方体的操作是可靠和平稳的，由于其精心设计的组件，构建是整洁的。当然，现在甚至还有[可以自己解决的魔方](https://hackaday.com/2018/09/24/self-solving-rubiks-cube/)。休息后的视频。

 [https://www.youtube.com/embed/xboPoVXxuZM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/xboPoVXxuZM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

