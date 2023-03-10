# 用慧鱼制造的取放机器人

> 原文：<https://hackaday.com/2019/07/30/pick-and-place-robot-built-with-fischertechnik/>

如果我们认为 Fichertechnik 只是孩子们的玩具，那就大错特错了。它也非常适合机器人控制系统的原型制作。[davidatfsg]最近参加了黑客日奖(Hackaday Prize)，[Delta Robot](https://hackaday.io/project/166794-delta-robot)，展示了如何实现复杂的机器人技术，而无需钻孔、切割、螺栓连接或焊接组件。额外的好处是，该机器可以完全拆卸非破坏性和重建一个新的和更好的设计，很少或没有浪费。

该项目使用 Arduino Mega 上运行的反向运动学从移动的传送带上拾取彩色物体，并将其放入各自的垃圾箱中。还有一个光学编码器用于调节传送带的速度，还有一个激光束用于感应传送带上的物体是否已经到达要拾取的正确位置。

并非每个组件都是现成的。[davidatfsg] 3D 打印了一个用于实际“挑选”的简单喷嘴，所需的真空是通过巧妙使用一对气缸和电磁操作空气阀产生的。

我们很确定这不会是 Hackaday 上最后一个使用[慧鱼](https://www.fischertechnik.de/en/products/playing/robotics)组件的项目，这是【大卫特 fsg】炮制的[第二个](https://hackaday.com/2018/04/20/a-polar-coordinate-cnc-plotter-even-descartes-could-love/)。休息后机器工作的视频！

 [https://www.youtube.com/embed/2Me_oyMifoU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/2Me_oyMifoU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/WYtq_7WfIS0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/WYtq_7WfIS0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2019](https://prize.supplyframe.com) is Sponsored by: [![Supplyframe](img/79a7db035b8a2b6c2b7b0895c45b7de8.png)](https://supplyframe.com/)  [![Digi-Key](img/ba094a14c430ab81591a2abdc54a5363.png)](https://hackaday.io/digikey)  [![Microchip](img/5023ef0b7ff1aee311cba9b54a3ac9fe.png)](https://hackaday.io/microchip)