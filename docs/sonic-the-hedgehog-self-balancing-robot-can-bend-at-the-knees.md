# 刺猬索尼克自平衡机器人可以弯曲膝盖

> 原文：<https://hackaday.com/2020/01/31/sonic-the-hedgehog-self-balancing-robot-can-bend-at-the-knees/>

对于任何进入机器人领域的人来说，建造自己的自平衡机器人都是必经之路。机器人大师[詹姆斯·布鲁顿]去过那里，做过那个，还收集了几件 t 恤。现在，他正在建造一个大型的刺猬索尼克自平衡机器人，它可以弯曲膝盖和臀部，允许它在转弯时倾斜，并处理不平坦的地形。请看休息后嵌入的第一个视频。

该机器人身高约 1 米，灵感来自波士顿动力公司的箱子搬运机器人 [Handle](https://hackaday.com/2017/02/27/i-am-science-fiction-incarnate-i-am-handle/) 。它的“骨架”由 20×20 的铝型材组成，用一堆 3D 打印的配件用 Sonic 标志性的蓝色和红色栓接在一起。车轮和轮胎也是 3D 打印的，由无刷电机通过齿形带驱动。膝盖/臀部机构由滚珠丝杠驱动，也由无刷电机驱动。

[詹姆斯]打算在腿部机构中实现一个主动减震系统，使用他在他的开放式狗机器人上尝试的相同技术。它的工作原理是将一个测压元件栓接到一个腿挤压件上，以感应它何时在负载下弯曲，然后启动膝盖机构来吸收力。他在 OpenDog 上的第一个系统版本使用 PWM 信号将称重传感器数据发送到主控制器，但腿上的电机在信号线中引起了足够的噪声，使其无法使用。从那以后，他开始试验 CAN 总线协议，这种协议是专门为在现代汽车这样的高噪声系统中可靠工作而设计的。如果他让它在这个声波机器人的两条腿上工作，他计划也在四足开放式狗上实现它。

这是来自[James]的另一个非常雄心勃勃的项目，我们真的很期待接下来的几期。在他的带领下，有了一系列复杂的项目，如全尺寸星球大战机器人系列，我们对成功寄予厚望。

 [https://www.youtube.com/embed/yF14N03rkS4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/yF14N03rkS4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

