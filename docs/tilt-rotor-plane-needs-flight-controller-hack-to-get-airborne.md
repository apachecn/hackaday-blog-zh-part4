# 倾转旋翼机需要飞行控制器破解才能起飞

> 原文：<https://hackaday.com/2018/11/06/tilt-rotor-plane-needs-flight-controller-hack-to-get-airborne/>

四轴飞行器的部分魅力在于建造和飞行它们所带来的挑战。由于需要复杂的传感器和计算能力才能离开地面，并且由于它们的大功率发动机，它们在飞行中似乎只能勉强控制。尽管有这些挑战，四轴飞行器飞行已经在许多方面被简化为实践，让爱好者寻找另一个挑战。

[汤姆·斯坦顿]正在挠他的创作之痒，这架无线电控制的倾转旋翼飞机带来了一些独特的问题和机遇。顾名思义，倾转旋翼机能够旋转它们的螺旋桨，并将它们从提供向前的推力转变为提供垂直的升力。通过旋翼提供升力，飞机能够悬停并执行垂直起飞和着陆(VTOL)；切换到推力模式，机翼为水平飞行提供升力。

[Tom]这种设计的实现看起来很简单——一根穿过机翼的翼梁支撑着 BLDC 发动机和推进器，通过伺服系统旋转 90°来转换飞机。机翼和尾翼上的标准操纵面负责水平飞行。实际上，获得现成的飞行控制器来处理转换是很棘手的。[Tom]最终添加了一个 Arduino 来拦截飞行控制器通常直接发送给伺服系统和速度控制的 PWM 信号，以提供平稳过渡所需的协调。下面的视频中的全部细节，以及一些测试飞行表明，遥控垂直起降飞机绝不是初学者的飞机。

[汤姆]这些天来证明了自己是一个文艺复兴时期的人。在[气动活塞发动机](https://hackaday.com/2017/11/20/acetone-smoothing-results-in-working-motor/)、[超平衡投石机](https://hackaday.com/2018/09/10/trebucheting-tennis-balls-at-124-mph/)和[弹出完美轮距](https://hackaday.com/2018/09/24/cheating-the-perfect-wheelie-with-sensors-and-servos/)之间，他似乎已经覆盖了所有的基础，并尽最大努力保持我们的小费线库存。

 [https://www.youtube.com/embed/gPEeCjVrTBw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/gPEeCjVrTBw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[baldpower]也不是一个没精打采的人。