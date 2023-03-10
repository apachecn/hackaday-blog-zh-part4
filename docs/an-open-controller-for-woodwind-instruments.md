# 木管乐器的开放式控制器

> 原文：<https://hackaday.com/2018/10/19/an-open-controller-for-woodwind-instruments/>

工程师、黑客和制造者肯定能制造出某种音乐小工具。他们将建造合成器，他们将建造航空电话，他们将采用水银延迟线存储器的想法，两个水听器，和一个装满水的很长的管子来建造现存最荒谬的延迟。他们似乎不能做的一件事是建立一个木管乐器 MIDI 控制器。这就是(乔丹)的用武之地。他创建了开放木管项目作为一个开放的可扩展接口，可以在连接到电脑时演奏萨克斯和单簧管。

[![](img/e7d6f5452d2aa61a4530b039b9e8ebf2.png)](https://hackaday.com/wp-content/uploads/2018/10/3275531433988291960.jpg)

Early prototype to test out variable resistive pressure pads

如果你想演奏 MIDI，有很多键盘、架子鼓、矩阵键盘甚至弦乐的选择。如果你想弹一个 MIDI 萨克斯，选择不多。例如，Keytars 比 MIDI 木管乐器控制器更受欢迎。[J.M.]正在用一个 MIDI 控制器改变这一点，它用电子学方法重新创造了电子飞机。

控制器本身使用一个加载了 ARM Cortex M4 的 Teensy 3.2，两个 MPR121 触摸控制器用于 24 通道的电容触摸功能，以及一个压力传感器来告诉计算机用户吹气的力度。所有这些都有效，[J.M.]有几个视频展示了他自制控制器的功能。这是一项伟大的工作，有几个扩展使它非常有趣:有可能添加 CV，以便它可以连接到模块化合成器，并且在构建中添加加速度计会产生一些非常有趣的效果。

看看下面的视频。

 [https://www.youtube.com/embed/SQb0_0ZK6nc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/SQb0_0ZK6nc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)