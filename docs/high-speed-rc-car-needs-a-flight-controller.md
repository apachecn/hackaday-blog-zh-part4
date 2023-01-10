# 高速遥控车需要飞行控制器

> 原文：<https://hackaday.com/2022/08/23/high-speed-rc-car-needs-a-flight-controller/>

地球上最快的地面车辆不是由车轮驱动，而是由飞机喷气发动机驱动。在创世界纪录的速度下，它们在限制速度的下压力和可能导致死亡和破坏的起飞之间的空气动力学剃刀边缘上运行。[rctestflight]想要看看让一辆遥控汽车以非常高的速度行驶需要什么，所以他建造了一辆[涵道风扇驱动的汽车](https://www.youtube.com/watch?v=mp5WJwT7HW0)，它带有空气动力学控制表面和飞机飞行控制器。

这种高速汽车建立在 1/14 比例的 RC 越野车的底盘上，由安装在非常长的空气动力学泡沫板壳上的 4 个 EDF(电动涵道风扇)提供动力。它还有一个飞机式的尾部，带有升降副翼和方向舵，使用 ArduPilot 飞行控制器在高速下进行稳定和控制。飞行控制器被设置成在滚转和偏航轴上稳定，在俯仰轴上只有固定的配平。

[rctestflight]让这辆车达到了 71 英里/小时(114 公里/小时)，这对大多数遥控汽车来说都很快，但远低于 202 英里/小时的遥控汽车速度纪录。仍然很难保持直线行驶，颠簸的道路当然也没有帮助。他希望在未来用更大的马达和高压电池再次挑战这一挑战。

 [https://www.youtube.com/embed/mp5WJwT7HW0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/mp5WJwT7HW0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



如果你想做的不仅仅是直线行驶，或者倒着驾驶，最大下压力是你的朋友。这可以通过[精心的空气动力学设计](https://hackaday.com/2021/12/21/ground-effect-aerodynamics-on-an-rc-car/)来实现，或者只是[加上风扇](https://hackaday.com/2021/05/23/rc-car-gets-fan-assisted-downforce-to-slay-teslas-0-60-times/)把车吸到地上。