# 自定义游戏杆构建指南应该为您指出正确的方向

> 原文：<https://hackaday.com/2021/09/08/custom-joystick-build-guide-should-point-you-in-the-right-direction/>

在过去的两年里，[benkster]一直在完善他们理想的飞行控制器。像许多人一样，他们从键盘和鼠标开始，最终转向操纵杆。虽然 HOTAS(手放在油门和操纵杆上——例如，输入就在侧面的轭式控制器)可能是下一个合乎逻辑的步骤，但这些东西成本太高。很自然，答案是建造一个，最好是花更少的钱。嘿，这是有可能的。

[![](img/c9b9c2cf61f5cb4168b9c947ca8e3fc6.png)](https://hackaday.com/wp-content/uploads/2021/09/joysticks-btns-slider.jpg) 这个设计从一个想法到一个纸板原型，再到一个木制外壳，再到后来的 3D 打印外壳。由于[benkster]在这一过程中学到了很多，他们希望用[一个全面的操纵杆设计/构建指南](https://hackaday.io/project/181309-a-guide-to-custom-joysticks)回馈社区，这样其他人就不必从零开始，被信息淹没。

[benkster]想要三个操纵杆、一堆大按钮、一个油门、一个显示组件状态的显示器(比如，3 号操纵杆现在是操纵杆还是 WASD 键盘？)，以及无处不在的身临其境的细节——你知道，一百万个按钮和开关让它有驾驶舱的感觉。[benkster]正在使用 Teensy 4 控制两个 3 轴操纵杆和一个 2 轴操纵杆。因为这对 Windows/DirectX 来说意味着太多的轴需要读入，所以 2 轴棒被用作 WASD 键盘。

本指南是一个很好的起点，尤其是对于那些可能对电子产品比较陌生的人。有许多类型的组件和与游戏杆世界之外相关的珍闻的很好的介绍。

你想要远离电脑的身临其境的飞行模拟？这里有一个可打印的基于弯曲的“棒”,它可以卡在你的 Xbox 控制器上并按下按钮。