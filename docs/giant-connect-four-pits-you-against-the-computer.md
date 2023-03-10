# 巨人连接四个坑你对电脑

> 原文：<https://hackaday.com/2018/09/26/giant-connect-four-pits-you-against-the-computer/>

您可以在软件中构建一个“连接四个”解算器，但这并不那么有趣。现在将同样的自动化应用到一个 15 英尺高的胶合板版本的经典棋盘游戏上，你就为视力范围内的每个人创造了一个微笑制造机。看看精通连接的多功能自动化机器人，这是本和乔纳森去年在从制造商博览会回家的路上想象出来的，并在今年的展览中展出。

 [![The game board](img/e6e6d7a2c4c911eddbaa72e6601aa590.png "giant-connect-four-in-use")](https://hackaday.com/2018/09/26/giant-connect-four-pits-you-against-the-computer/giant-connect-four-in-use/) The game board [![The scoreboard](img/d5f5bb7e8dacf472d074ebfa98ea188b.png "giant-connect-four-scoreboard")](https://hackaday.com/2018/09/26/giant-connect-four-pits-you-against-the-computer/giant-connect-four-scoreboard/) The scoreboard

在物理方面，他们非常有创意地举起圆盘，并把它们分类到由游戏的软件大脑选择的栏中。链条沿着一边移动，每隔几英尺就有一个手指。手指沿着通道移动，提起圆盘。那些手指是几个螺栓，用一些金属填充物，全部用环氧树脂粘合成一个固体单元。

 [![Zoom in and you can see the solenoids controlling the disc drop](img/6da89c4a4f624f9cb08efa9d34e3160f.png "connect-four-solenoids")](https://hackaday.com/2018/09/26/giant-connect-four-pits-you-against-the-computer/connect-four-solenoids/) Zoom in and you can see the solenoids controlling the disc drop [![The chain for lifting discs](img/116fca86b5c4028d1bce76b9976daf47.png "giant-connect-four-chain")](https://hackaday.com/2018/09/26/giant-connect-four-pits-you-against-the-computer/giant-connect-four-chain/) The chain for lifting discs [![Arduino, router, and power supply](img/f654c7a72dc497de2eb085b95d274104.png "giant-connect-four-electronics")](https://hackaday.com/2018/09/26/giant-connect-four-pits-you-against-the-computer/giant-connect-four-electronics/) Arduino, router, and power supply

在光盘升降机的顶部，以及游戏板中每一列的顶部位置，都有红外反射传感器，这些传感器向驱动硬件的 Arduino 发送反馈。这被证明是集会前一天设置的一个主要问题。反射传感器只是发射红外线，并不使用载波信号。在阳光直射下，探测器一直处于跳闸状态。经过反复试验，传感器的逻辑被翻转，通过将黑色塑料放在电路板的顶行后面，并将管道胶带放在红外发射器上，来检测阳光的缺乏。

 [![Detail of the disc elevator](img/c480b6fa9906cb80c3079e20de744382.png "giant-connect-four-discs-in-elevator")](https://hackaday.com/2018/09/26/giant-connect-four-pits-you-against-the-computer/giant-connect-four-discs-in-elevator/) Detail of the disc elevator [![This thing was a huge build to transport from Philly](img/8481f876e47d1070fe6e9472b5ae6a59.png "giant-connect-four-setup")](https://hackaday.com/2018/09/26/giant-connect-four-pits-you-against-the-computer/giant-connect-four-setup/) This thing was a huge build to transport from Philly

系统中集成了路由器和笔记本电脑。Arduino 向笔记本电脑上的软件发出 HTTP 请求。除了确定下一步应该走哪里，笔记本电脑还连接到一个大屏幕，显示游戏板的当前状态。这是一场面对面的，人类对机器的游戏。人类玩家使用一个油漆滚筒从棋盘顶部放下他们的圆盘，油漆滚筒钩住圆盘中心的一个孔。这样，播放器的光盘通过传感器，触发机器的下一步行动。

这是一个聪明的建筑，由于其庞大的规模，他们能够将它从费城带到展会上真是太棒了。不要错过休息后展示这个游戏巨头的乐趣和兴奋的视频。

 [https://www.youtube.com/embed/u6YReH6S19g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/u6YReH6S19g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

