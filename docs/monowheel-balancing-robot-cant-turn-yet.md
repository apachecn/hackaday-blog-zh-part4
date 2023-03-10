# 独轮平衡机器人还不会转弯

> 原文：<https://hackaday.com/2021/07/24/monowheel-balancing-robot-cant-turn-yet/>

自平衡机器人已经成为一个常见的爱好项目，它们通常需要两个轮子才能工作。[詹姆斯·布鲁顿]已经设法通过增加陀螺稳定来使[单轮平衡机器人](https://www.youtube.com/watch?v=fNQkZ7MmGio)。

[詹姆斯]已经做了其他自平衡机器人，如他的[声波机器人](https://hackaday.com/2020/02/26/sonic-the-self-balancing-robot-face-plants-and-the-challenges-of-sensor-integration/)，但最近开始试验[陀螺稳定](https://hackaday.com/2021/05/17/actively-balancing-a-robot-with-a-gyroscope/)。在那个项目中，他提出了将两种稳定方法结合起来创造一个单轮机器人的想法，并贯彻了这个想法。车轮由无刷电机驱动，通常围绕车轮轴线稳定。通过倾斜一对沉重的旋转车轮，利用一种称为回转进动的现象实现左右平衡。这不要与反作用轮混淆，反作用轮使用转动惯量进行控制。似乎启动陀螺仪也会影响前后稳定性，所以此时机器人不会停留在一个地方。[James]计划在软件中实现第二个观察控制器来解决这个问题。

这个机器人的另一个挑战是它现在不能转弯。陀螺仪没有处于正确的方向来实现绕垂直轴的旋转，并且改变它们的方向会导致其他问题。一个像直升机尾桨一样工作的风扇是一种选择，顶部的反作用轮也可能起作用。我们倾向于反作用轮的想法。每个轴有不同的机械控制机制将使它成为一个非常有趣的机器人。

 [https://www.youtube.com/embed/fNQkZ7MmGio?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/fNQkZ7MmGio?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

