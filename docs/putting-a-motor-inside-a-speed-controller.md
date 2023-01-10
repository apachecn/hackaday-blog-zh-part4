# 将电机放入速度控制器中

> 原文：<https://hackaday.com/2018/10/23/putting-a-motor-inside-a-speed-controller/>

今年我们见过的最有趣的黑客之一是[Carl]用多氯联苯制造马达的实验。老实说，令人惊讶的是以前没有人这样做过——无刷电机只是一些线圈和几块磁铁；任何人都可以将一些线圈变成轨迹，并制作一个可以容纳几块磁铁的 3D 打印。这一最新进展完全是另一回事。[集电机和电子调速器于一身](https://www.youtube.com/watch?v=4cdVpoWTC_c)。

这个项目是[【卡尔】的 PCB 电机项目](https://hackaday.io/project/39494-pcb-motor)的延续，该项目始于他在电路板上为无刷电机布线线圈。之前，我们已经看到[卡尔]的马达[在一个小型爱好 ESC /马达控制器的帮助下自行旋转，该控制器是为模型飞机和无人机设计的。这一次，我们得到了不同的东西。这是一个完整的控制器和电机，集成到一个单一的 PCB。](https://hackaday.com/2018/05/12/the-current-advances-of-pcb-motors/)

这是一个非常非常小的电机和 ESC 组合。电机驱动器是一个 3x3mm QFN 封装，其他大部分元件是 0201。主要部分是[一个非常小的三半桥电机驱动器](https://www.st.com/en/motor-drivers/stspin230.html)和一个 PIC16F 微控制器。该 PIC 读取霍尔传感器来检测电机的速度，只需三个引脚——电源、接地和一个 PWM 引脚——该电机就可以以设定的速度旋转。

这个项目的未来目标是让它像任何其他爱好 ESC 一样工作——只需将其插入伺服控制器，然后让它撕裂。由于这种集成 PCB 的电机只需要三个连接，我们正在寻找一个伟大的工具来增加任何项目的运动和旋转。这太棒了，我们迫不及待地想在机器人、玩具和其他家居用品中看到类似的东西。

 [https://www.youtube.com/embed/tbXLc8F3HFg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/tbXLc8F3HFg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/4cdVpoWTC_c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/4cdVpoWTC_c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

