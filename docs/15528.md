# 将保时捷 944 改装成 MAF

> 原文：<https://hackaday.com/2022/12/02/converting-a-porsche-944-to-run-a-maf/>

电子燃油喷射是发动机控制的一大飞跃。然而，早期的实现经常留下一些不尽人意的地方。[Rob]和他的保时捷 944 就是这种情况，它依赖于老式的机械式空气流量计(AFM)。他决定用一个现代质量空气流量(MAF)传感器来代替它，并在网上记录了这个过程。

![](img/27a00356ceb11630497c40eb633032d3.png)

The output of the sensors was compared with a rig built using a vacuum cleaner to create air flow.

原子力显微镜通常是替换旧汽车的目标。它们通常基于一个挡板，该挡板将电位计游标移过多年来磨损的碳迹线。在某些情况下，它们还会限制空气流动，从而限制性能。MAF 传感器通过热线测量空气流量。维持电线温度所需的电流量表示流过传感器的空气量。它们限制更少，而且很容易获得，因为它们现在被用在许多汽车上。

用 MAF 代替原子力显微镜需要一个电路来模拟原子力显微镜的输出。[Rob]使用 STM32 Cortex-M0 读取 MAF，然后通过 PWM 和低通滤波器将相关电压输出到保时捷的发动机计算机。为了找出如何映射 MAF 的输出以匹配原子力显微镜，[【Rob】建造了一个装置](https://robprojects.github.io/porsche944/2020/04/12/afm2.html)将空气依次吹过两个设备，并在示波器上测量它们的输出。该数据用于[对 STM32](https://robprojects.github.io/porsche944/2022/02/01/afm3.html) 编程，以针对给定的 MAF 信号输出正确的仿真 AFM 电压。

这是[Rob]的一个伟大作品，他的保时捷在新零件上快乐地运行。[在](https://hackaday.com/2019/08/08/putting-carbs-on-a-miata-because-its-awesome/)之前，我们也看到过对其他汽车的类似攻击！休息后的视频。

 [https://www.youtube.com/embed/9davtq7FP1U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/9davtq7FP1U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

