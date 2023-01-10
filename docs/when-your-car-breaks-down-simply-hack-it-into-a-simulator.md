# 当你的车抛锚时，只要把它黑进模拟器就行了

> 原文：<https://hackaday.com/2019/09/27/when-your-car-breaks-down-simply-hack-it-into-a-simulator/>

当[尼桑特]的斯巴鲁 BRZ 突然停下来时，他对等待安装新发动机感到难过。幸运的是，与此同时，他通过把它黑进汽车模拟器让自己振作起来。这将有一个额外的好处，即不仅限于在不幸事故发生的[路 Atlanta](https://en.wikipedia.org/wiki/Road_Atlanta) 上驾驶，而是可以在 Forza 和类似的赛车游戏上驾驶。

从理论上看，这似乎相当简单:只需接入汽车的 CAN 总线，获取转向、油门、刹车和其他信号，将其转换为游戏机或 PC 可以处理的东西，然后就可以参加比赛了。这里的个人电脑安装绝对是最便宜和最简单的，只需要一个零件:Dash 套件下的一个[Macchina M2](https://www.macchina.cc/m2-introduction)(97.50 美元)。XBox 需要价值超过 200 美元的零件，包括前面提到的 Macchina 零件、XBox 自适应控制器和其他一些零件。当然还有一辆车。

![https://www.notion.so/image/https%3A%2F%2Fs3-us-west-2.amazonaws.com%2Fsecure.notion-static.com%2Fd49697c6-29ae-4b4d-a27b-e2da019d32de%2FUntitled.png?table=block&id=ed4e1bf2-91c6-4494-8e0f-f10964620869&width=5120&cache=v2](img/a3d0a28ea8467e5c5a999c7244afd27b.png)

Macchina M2 是通过 OBD2 端口监听 CAN 流量的部分，将其转换为类似 USB HID 游戏手柄的东西。所以这都是即插即用的问题，对吗？没那么快。每辆车都使用自己的基于 CAN 的系统，具有不同的外设和地址。这意味着，随着 Macchina M2 收购，[尼桑特]的第一个任务是逆向工程的汽车控制 CAN 信号。

在这一点上，个人电脑方面的故事已经基本结束，但 XBox One 主机被设计为只接受官方外设。这里的一个漏洞是为残疾人设计的[自适应控制器](https://en.wikipedia.org/wiki/Xbox_Adaptive_Controller)，它允许使用替代输入。这也使得可以将汽车用作 XBox One 控制器，这是一个有趣的副作用。

XBox 版本的最后一个问题是，自适应控制器不允许从其 USB 端口控制触发器，因此他们必须通过附加电路使用控制器上的 3.5 毫米(模拟)输入来添加此功能。这样一来，他们就准备尝试一些游戏了。

 [https://www.youtube.com/embed/VkPxM4QOLWA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/VkPxM4QOLWA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

