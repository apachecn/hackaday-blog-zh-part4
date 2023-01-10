# 3D 打印遥控潜水器是许多经验教训的结果

> 原文：<https://hackaday.com/2022/11/02/3d-printed-rov-is-the-result-of-many-lessons-learned/>

建造水下遥控潜水器(ROV)始终是一个挑战，使其防水通常是一个主要障碍。[Filip bu awa]和[Piotr Domanowski]花了四年时间和 14 个原型进行迭代，创造了 CPS 5，这是一种 3D 打印的 ROV，潜在深度可达 85 米。

众所周知，FDM 3D 打印很难防水，这要归功于各层之间的微孔。有一些方法可以减轻这种情况，但它们都有局限性。没有试图使 CPS 5 的印刷外部防水，而是将电子设备和相机封装在一对密封的丙烯酸管中。端盖仍然是 3D 打印的，但实际上只是填充了环氧树脂的薄壁容器。布线通道也用环氧树脂密封，但[菲利普]和[彼得亚雷]艰难地认识到，绝缘电线也可以作为水进入的管道。他们通过在环氧树脂填充的通道中为每根导线增加一个开放的焊点来解决这个问题。

对于推进，姿态和深度控制，CPS 5 有五个无刷无人机马达，配有 3D 打印的螺旋桨，只要你密封连接器，它们就不会受到水的影响。控制电子设备由 PixHawk 飞行控制器和 Raspberry Pi 4 组成，用于处理通信和笔记本电脑的视频流。IMU 和水压传感器还可以实现水下自动调平和深度保持。像大多数遥控潜水器一样，它使用系绳进行通信，在这种情况下，这是一条带有防水连接器的以太网电缆。

丙烯酸管是遥控潜水器的一个受欢迎的电子容器，我们已经看到了 [RC Subnautica 潜艇](https://hackaday.com/2020/08/06/scratch-built-subnautica-sub-explores-the-pool/)、[乐高潜艇](https://hackaday.com/2022/07/18/how-to-become-a-lego-submariner/)和 Hackaday 获奖的[水下滑翔机](https://hackaday.com/2017/11/20/an-interview-with-alex-williams-grand-prize-winner/)。

 [https://www.youtube.com/embed/arTLho86huQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/arTLho86huQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

