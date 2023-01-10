# 大翼尖驱动的直升机转弯非常慢

> 原文：<https://hackaday.com/2022/08/08/large-tip-driven-copter-turns-very-slowly/>

选择任何飞机的螺旋桨尺寸，尤其是垂直起降飞机，这是尺寸和转速之间的权衡。您可以缓慢移动大量空气，也可以快速移动少量空气。对于许多应用来说，小而快往往是最实用的，但如果你像[amazingdiyprojects]一样跳出框框思考，你可以[建造一个巨大的螺旋桨，让它以每秒一转的速度飞行](https://www.youtube.com/watch?v=JfP7955XipY)。(视频，嵌入休息下方。)

大型螺旋桨的挑战之一是其高扭矩要求。为了解决这个问题，[amazingdiyprojects]使用带有螺旋桨的电动机从顶端驱动直径为 5 米的螺旋桨。叶片是简单的焊接铝框架，覆盖着热缩包装带，用金属丝加固。

飞行控制器自带电池，通过抵消一个小型 DC 发动机的旋转来防止叶片旋转。每个叶片都配备了一个伺服驱动的控制表面，它可以根据叶片的径向位置调整偏转，从而进行滚动和俯仰控制。

[amazingdiyprojects]控件设置非常有创意，但有些不精确。他没有尝试编写定制的控制方案，而是为六轴直升机配置了旧的 KK2.15HC 飞行控制器。每个控制伺服的 PWM 信号通过一个有六个扇区的整流盘传送，每个扇区对应虚拟直升机的一个马达。这意味着每个伺服开关之间的六个不同的 PWM 通道在其旋转。为了补偿频道切换时的延迟，[amazingdiyprojects]必须调整换向器圆盘的偏移量，否则它会转向错误的方向。在第二次试飞阶段调整飞行控制器设置后，控制权限得到了改善，尽管在响应方面仍然非常温顺。

[amazingdiyprojects]对巨型垂直起降飞机并不陌生，他曾制造并驾驶过自己的载人无人机，由内燃和 T2 电动机驱动。这种最新的飞行器与[【尼古拉斯·雷姆】的纺纱机](https://hackaday.com/2022/07/24/turn-drone-into-a-large-propeller-to-increase-hover-efficiency/)非常相似，也许能够利用控制系统。

 [https://www.youtube.com/embed/JfP7955XipY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/JfP7955XipY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/07jEAaAj1VA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/07jEAaAj1VA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

