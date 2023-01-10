# 使用四轴飞行器控制软件的垂直起落飞机尾翼

> 原文：<https://hackaday.com/2021/08/02/vtol-tailsitter-flies-with-quadcopter-control-software/>

四轴飞行器在机动性和缓慢稳定的飞行方面非常出色，但这是以效率为代价的。[彼得·雷塞克]的迷你 QBIT 四旋翼双翼飞机带来了固定翼飞机的一些效率，没有通常与垂直起降飞机相关的所有复杂性。

迷你 QBIT 只是一架 3 英寸的迷你四轴飞行器，在发动机下方安装了一对机翼，使其成为一架“tailsitter”垂直起降飞机。机翼和鼻锥使用磁铁附着在 3D 打印的框架上，这使得它们可以在碰撞中弹出。机翼上不需要操纵面，因为所有需要的操纵都是由马达完成的。这个 QBIT 是基于彼得在马里兰大学参与的一个研究项目。2017 年的论文称，测试飞机在向前飞行时比悬停时节省了 68%的电力。

(编者注:[ [彼得](https://www.researchgate.net/profile/Peter-Ryseck) ]直接联系了我们，[他得到了一份关于飞机](https://www.researchgate.net/publication/348751087_Experimental_Flight_Testing_of_Wing_Configurations_for_High-Speed_Mini_Quadrotor_Biplane_Tail-sitter)的更新的论文。)

让飞行控制器从悬停平稳过渡到向前飞行可能非常棘手，但 QBIT 使用运行 Betaflight 的普通四轴飞行器飞行控制器做到了这一点。四轴飞行器在自动调平模式(角度模式)下悬停，并切换到 acro 模式进行向前飞行。然而，当无人机俯仰向前飞行时，滚动轴变成偏航轴，偏航轴变成反向滚动轴。为了补偿这一点，控制器设置为通过开关切换这两个通道。对于 FPV 飞行，QBIT 使用两个摄像机用于两种不同的模式，每个都有自己的屏幕显示(OSD)。飞行控制器被配置成使用相同的模式开关来改变摄像机馈送和 OSD。

[彼得]正在他的网站上为 V2 出售零件和 STL 文件，但是你可以免费下载 V1 文件。然而，控制设置实际上是这个项目的定义特性，任何人都可以在他们自己的构建中实现。

对于另一个简单的垂直起降项目，看看【尼古拉斯·雷姆】的 [F-35](https://hackaday.com/2021/07/15/foam-f-35-learns-to-hover/) ，它运行在他的 [dRehmFlight](https://hackaday.com/2021/02/15/drehmflight-customizable-flight-stabilisation-for-your-weird-flying-contraptions/) 飞行控制软件上。

 [https://www.youtube.com/embed/8UOTyEGb7qE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/8UOTyEGb7qE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

