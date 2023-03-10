# 通过这个方便的分线点，尝试 SFP 模块

> 原文：<https://hackaday.com/2021/02/13/experiment-with-sfp-modules-with-this-handy-breakout/>

虽然大多数家庭网络硬件都带有出厂预装的网络端口，但工业级设备通常更加通用。通过使用小型可插拔或 SFP 等标准，网络交换机可以通过简单地交换收发器来用于各种传输介质。这些网络设备通常处理通过光纤传输以太网的细节，对于那些热衷于实验的人来说，这种突破可能会派上用场。

该板设计配有一个 SFP 插座，允许插入各种兼容的接收器进行实验。采用差分信号的标准，电路板带有硬件，允许收发器采用单端信号供电，[但也有差分版本可用](http://osmocom.org/projects/misc-hardware/wiki/Sfp-breakout)。该板可用于在以太网之外的光纤上传输不同的信号，或用作通过 I2C 重新编程 SFP 模块的简单方法。后者可用于避开试图锁定通用收发器模块的网络交换机中的 DRM。

对于光纤修补者和网络管理员来说，这是一个有用的硬件。如果你正在家里构建自己的 10 千兆网络，你可能会发现它很有用！