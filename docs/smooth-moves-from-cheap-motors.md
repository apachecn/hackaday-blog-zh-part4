# 廉价发动机的平稳运行

> 原文：<https://hackaday.com/2018/11/16/smooth-moves-from-cheap-motors/>

制造一台电动马达并不难，在技术上也不具有挑战性，但这些马达的控制能力很差。步进电机通常用于需要高精度的应用中，但为电机增加这一功能会增加复杂性，从而增加成本。有一个 3 美元的小型步进电机可用，但这种电机的缺点是，它并不完全是汽车中的凯迪拉克，也没有打算成为。不过，通过一些哄骗，【T-Kuhn】[能够从这个小而便宜的马达](https://electrondust.com/2018/11/11/esp-32-micro-robot-arm/)中得到很多。

为了测试马达，[T-Kuhn]制造了一个小型机械臂。他开始编写自己的脉冲生成算法，模仿正弦波，以平滑电机的运动。不过，Arduino 的速度还不足以完成这些计算，所以他升级到使用 ESP32。他也能够自己实现反向运动学。针对特定平台和电机类型的所有这些工作的结果是一个机器人手臂，它具有非常低的成本，但提供更昂贵的硬件的性能。

机器人手臂也是由[T-Kuhn]建造的，如果你需要一个低成本的机器人手臂或一个好的步进电机控制器，可以在项目网站上找到该建造的所有细节，以及所有的原理图和代码。还有许多其他方法可以充分利用其他类型的低成本电机。

 [https://www.youtube.com/embed/9MMsvZLFsI4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/9MMsvZLFsI4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

