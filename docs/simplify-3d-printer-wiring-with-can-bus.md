# 通过 CAN 总线简化 3D 打印机布线

> 原文：<https://hackaday.com/2021/11/03/simplify-3d-printer-wiring-with-can-bus/>

[mark]在观察一台典型的 3D 打印机的所有线路时，产生了一个有趣的想法；使用 CAN 总线。有很多电线连接到挤出机组件，在大多数设计中，这东西以相当快的速度飞来飞去。您已经连接了加热器、风扇电源、挤出机电机的四根电线、热敏电阻传感器电线。你明白了。很多电线。更糟糕的是，它们都绕着轴运动，如果由于应变消除不良而在两端发生故障，或者导体本身断裂，那么可能会发生各种有趣的故障。如果热端热敏电阻连接开路，通常不会发生损坏，但温度控制会失控，您的打印会失败。

现在，如果您将驱动和控制挤出机所需的电子设备直接推到移动体本身上，并通过 [CAN 总线](https://en.wikipedia.org/wiki/CAN_bus)连接到主打印机电子设备，您就可以用区区四根电线完成整个移动互连。是的，你需要另一个 PCB 组件，这增加了成本，但也简化了控制端的电子器件，因此可以节省一些成本。[mark]使用了 CAN 总线，这是因为它可用于现代微控制器，而且由于其汽车和工业传统，其设计坚固耐用。当你想到它时，这是一件相当明显的事情，我们不确定为什么我们以前没有看到它。

如果你想深入了解细节，GitHub 项目已经准备好了原理图和代码。

 [https://www.youtube.com/embed/fLWfx6dVZus?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/fLWfx6dVZus?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

