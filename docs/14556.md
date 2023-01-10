# 优化遥控倾转旋翼垂直起落飞机

> 原文：<https://hackaday.com/2022/08/22/optimising-a-rc-tilt-rotor-vtol/>

在建造固定翼垂直起降无人机时，有多种可能的电机配置可供选择，但很少有人采用 V-22 鱼鹰使用的双电机倾转旋翼方法。然而，对于像[汤姆·斯坦顿]这样的军用飞机爱好者来说，它仍然是一种流行的 DIY 无人机。他最近建造了他的[第五倾转旋翼垂直起落飞机](https://www.youtube.com/watch?v=XPXN0QejqM0)，并对开发过程进行了出色的观察。休息后的视频。

任何小型倾转旋翼机的关键部件是倾转机构和飞行控制器。[Tom]的倾斜机构使用高速、高扭矩的伺服系统，通过 3D 打印的齿轮机构旋转电机支架。这意味着伺服系统不需要承受电机的全部负载，传动装置可以针对扭矩和速度进行优化。[Tom]还在向前飞行期间使用倾斜马达进行偏航和滚转控制，这使他能够消除除升降舵之外的所有其他常规控制表面。

飞行控制器由一个 Teensy 和陀螺仪/加速度计模块组成，运行 [dRehmFlight 飞行稳定固件](https://hackaday.com/2021/02/15/drehmflight-customizable-flight-stabilisation-for-your-weird-flying-contraptions/)。dRehmflight 是专门为适应各种各样的实验性飞机配置而设计的，它允许[汤姆]第一次尝试就升空。

碳纤维管用于机翼梁和尾梁，并用螺栓固定在由 3D 打印支架和 1 毫米玻璃纤维增强塑料板制成的机身上。[Tom]选择 NACA 4412 翼型机翼是因为它在大迎角范围内的线性升力系数，允许悬停和前飞之间的平稳过渡。机翼是用[轻质发泡 PLA](https://hackaday.com/2020/02/17/bubbly-filament-works-better-than-you-think/)(LW-PLA)3D 打印的，这需要一些精心设计才能获得高质量的打印。LW-PLA 的发泡意味着如果它停止挤压，它将总是会渗出，所以[Tom]使用切片机的“花瓶模式”设计了将在一条连续线上挤压的机翼表面和内部肋。亚光黑色的翅膀在阳光下开始扭曲，这是通过将翅膀重新打印成白色解决的。

飞机在两种飞行模式下表现良好，但在转换回悬停状态时减速有些困难。这是对先前版本的重大改进，先前版本在悬停时缺乏偏航控制，在向前飞行时有点不稳定。

 [https://www.youtube.com/embed/XPXN0QejqM0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/XPXN0QejqM0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

